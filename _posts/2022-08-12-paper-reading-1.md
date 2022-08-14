---
title: 'Paper Reading:Assisting Example-based API Misuse Detection via Complementary Artificial Examples.'
date: 2022-08-12
permalink: /posts/2022/08/paper-reading-1/
tags:
  - software reuse
  - empirical software engineering
  - API-misuse detection
---

## Brief Summary
The paper improves the user experience of the misuse detection tool(named MuDect) because fewer false positive results would be given after applying our artificial examples. The experiment of this paper depends heavily on manual experience and checking, and the authors propose 5 patterns to generate more valid API usage examples to avoid potential misjudgment.

## Positive Aspects
1.	A very careful manual checking and huge Java experience requirement in this experiment.
It can be seen in three parts. Firstly, the authors put the 384 detected API misuses into a total of four categories manually and they find only 108 of them could be fixed by providing more usage examples. Secondly, the author proposed 5 patterns based on their personal experience. Thirdly, after applying the methodology to test projects, the result of precision and recall needs to be checked manually. I think this kind of effort is a valuable asset. To be honest, my previous work also requires a lot of manual checking and I know its hardness.

2.	The passage provides us with a new thinking way. Many people choose to enhance the framework of the state-of-art tool to achieve better results, but this paper does not. It chooses to enhance the quality of its input(giving more usage examples). Like many ML frameworks today, I think the profit of improving the quality of input data is bigger than optimizing parameters. This also gives us a potential topic, if we can enhance the input data of neural networks, maybe it will slow the appearance of overfitting and get a training model with better quality?

3.	The algorithm of each detection strategy is very simple and useful. They are not very complete and it is more based on experience. Actually, it is unrealistic to apply a complete algorithm in a real industrial project. I think this paper makes a good tradeoff in the effectiveness of the algorithm and the time&space limit.


## Limitations
1.	As mentioned in the paper, it only lowers the number of false-positive but does not improve the number of true-positive. In my opinion, I think improving the number of true-positive has more meaning. Even if some false-positive detections exist, they can be moved just by double checking, but if we want to discover some more true-positive, that’s more difficult.

2.	I am worried about the generality of the selection of projects. In my own opinion, different projects have different features. For example, Apache-commons-math will use a lot of Java Math packages while Apache-commons-io will use a lot of API in Java IO. I do not think the 5 patterns can be applied to various projects even if the authors claimed that they get good results in the test set.

3.	Followed by limitation 2, I think an unsupervised clustering algorithm needs to be considered to generate the patterns of complementary artificial examples due to the variety of Java projects.It can also solve a lot of humanic energy.
