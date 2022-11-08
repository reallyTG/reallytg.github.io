---
title: "Towards a Type System for R"
collection: publications
permalink: /publication/2019-07-19-towards-a-ts-for-R
excerpt: 'This paper describes our initial exploration into the challenges of building a static type system for R.'
date: 2019-07-19
venue: 'ICOOOLPS (ECOOP)'
paperurl: 'http://reallytg.github.io/files/papers/towards-ts-for-r.pdf'
citation: 'Alexi Turcotte and Jan Vitek. 2019. Reasoning About Foreign Function Interfaces Without Modelling the Foreign Language. <i>Proceedings of the 14th Workshop on Implementation, Compilation, Optimization of Object-Oriented Languages, Programs and Systems</i>, ICOOOLPS, Article 4 (July 2019), 5 pages.'
---

R is a fascinating language: It is dynamically typed, vectorized, both lazy and side-effecting, and it fosters an interactive style of programming. This unique combination of features makes it easy to use, but prone to errors and strange behaviour. R is the tool of choice for many data analysts, and our aim is to empower them with a language that is not simply easy to use, but easy to use well, so as to increase their confidence in the data analyses they undertake. To that end, we are developing a type system for R that is simple enough to be attractive to programmers while being expressive enough to capture existing programming paradigms. In this paper, we outline past, present, and future work as we build up to a type system for R.