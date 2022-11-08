---
title: "The VM Already Knew That"
collection: publications
permalink: /publication/2017-10-12-vm-already-knew-that
excerpt: 'Virtual machines are already performing many of the type checks demanded by sound gradual type systems, and eliminating redundant checks significantly improves performance.'
date: 2017-10-12
venue: 'OOPSLA'
paperurl: 'http://reallytg.github.io/files/papers/oopsla17-oopsla98.pdf'
citation: 'Gregor Richards, Ellen Arteca, and Alexi Turcotte. 2017. The VM Already Knew That: Leveraging Compile-Time Knowledge to Optimize Gradual Typing. <i>Proc. ACM Program. Lang. 1</i>, OOPSLA, Article 55 (October 2017), 27 pages.'
---

Programmers in dynamic languages wishing to constrain and understand the behavior of their programs may turn to gradually-typed languages, which allow types to be specified optionally and check values at the boundary between dynamic and static code. 
Unfortunately, the performance cost of these run-time checks can be severe, slowing down execution by at least 10x when checks are present.
Modern virtual machines (VMs) for dynamic languages use speculative techniques to improve performance: If a particular value was seen once,
it is likely that similar values will be seen in the future. 
They combine optimization-relevant properties of values into cacheable "shapes", then use a single shape check to subsume checks for each property. 
Values with the same memory layout or the same field types have the same shape. 
This greatly reduces the amount of type checking that needs to be performed at run-time to execute dynamic code. 
While very valuable to the VM’s optimization, these checks do little to benefit the programmer aside from improving performance. 
We present in this paper a design for intrinsic object contracts, which makes the obligations of gradually-typed languages’
type checks an intrinsic part of object shapes, and thus can subsume run-time type checks into existing shape checks, eliminating redundant checks entirely. 
With an implementation on a VM for JavaScript used as a target for SafeTypeScript’s soundness guarantees, we demonstrate slowdown averaging 7% in fully-typed code relative to unchecked code, and no more than 45% in pessimal configurations.

[Download paper here](http://reallytg.github.io/files/papers/oopsla17-oopsla98.pdf)
