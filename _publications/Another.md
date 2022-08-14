---
title: "Assertions in Intelligent Test Generation May Be Unreliable: A
Study on Method Purity Changes in Java Releases"
collection: publications
permalink: /publication/Another
excerpt: '![](https://runzeyu1995.github.io/files/Another/structure.png) Intelligent test generation techniques, such as EvoSuite, rely on the
identification of method purity. Method purity indicates whether
executing a method is free of side effects. A method is pure if the
state of any object seen by the caller of the method never changes.
Identifying method purity can help developers understand program
behaviors in many tasks, such as assertion generation for regression
testing, path condition inference in static analysis, and state query
in synthesis-based program repair. These tasks can be simplified
via applying method purity since pure methods cannot modify
object states; thus, arbitrarily calling pure methods cannot disturb
the current program behaviors. However, method purity can be
changed. For instance, in regression testing, purity based assertion
generation is unreliable if a pure method is changed into an impure
one. In this paper, we conduct an exploratory study on the changes
of method purity in Java releases. We refer to such changes as
method purity reversals. We examine method purity reversals in 282
pairs of Java releases from 10 open-source projects. Our study shows
that an originally pure method can be changed into an impure one
in the next release and vice versa. Such changes are infrequent but
indeed exist. Our study reveals and analyzes the existence of method
purity reversals; the method purity reversals should be avoided to
reduce the risk to the reliability of intelligent test generation.'
date: 2021-10-02
venue: 'Under Review'
---

## Abstract
Intelligent test generation techniques, such as EvoSuite, rely on the
identification of method purity. Method purity indicates whether
executing a method is free of side effects. A method is pure if the
state of any object seen by the caller of the method never changes.
Identifying method purity can help developers understand program
behaviors in many tasks, such as assertion generation for regression
testing, path condition inference in static analysis, and state query
in synthesis-based program repair. These tasks can be simplified
via applying method purity since pure methods cannot modify
object states; thus, arbitrarily calling pure methods cannot disturb
the current program behaviors. However, method purity can be
changed. For instance, in regression testing, purity based assertion
generation is unreliable if a pure method is changed into an impure
one. In this paper, we conduct an exploratory study on the changes
of method purity in Java releases. We refer to such changes as
method purity reversals. We examine method purity reversals in 282
pairs of Java releases from 10 open-source projects. Our study shows
that an originally pure method can be changed into an impure one
in the next release and vice versa. Such changes are infrequent but
indeed exist. Our study reveals and analyzes the existence of method
purity reversals; the method purity reversals should be avoided to
reduce the risk to the reliability of intelligent test generation.