---
title: "Remediating Superfluous Re-Rendering in React Applications"
collection: publications
permalink: /publication/2026-05-15-re-rendering
excerpt: 'React is a ubiquitous front-end JavaScript library that pitches a smart mechanism to determine how much of a web page needs to be re-rendered when a change occurs. There are a few pitfalls that developers can fall into when developing such applications, and in this work we propose a set of anti-patterns and fixes to remediate these common isues.'
date: 2026-05-15
venue: 'ICSE'
paperurl: 'http://reallytg.github.io/files/papers/icse_26_rerendering.pdf'
citation: 'Farideh Khalili and Satyajit Gokhale, Alexi Turcotte, Dale Xu, and Frank Tip. <i>Remediating Superfluous Re-Rendering in React Applications</i> In Proceedings of the 48th International Conference on Software Engineering (ICSE). Association for Computing Machinery, New York, NY, USA. More information to come.'
---

React is an extremely popular framework for constructing user
interfaces (UIs). A React UI is organized as a tree of components,
each of which is defined by a function that returns a literal written
in JSX, a syntactic extension of JavaScript consisting of a combi-
nation of XML tags, executable JavaScript code, and references to
sub-components. React supports incremental re-rendering by main-
taining an in-memory representation of a web page’s Document
Object Model (DOM) and automatically calculating a set of minimal
changes that must be applied to the DOM when state changes occur.

However, React’s semantics are complex and subtle, and program-
mers often write code that gives rise to unnecessary re-rendering,
which hurts performance and responsiveness. We identify 5 React
anti-patterns that give rise to unnecessary re-rendering, present a
static analysis for detecting them, and rewrite rules that suggest
how to refactor the code to improve rendering performance. The
static analysis is potentially unsound, so developers should carefully
review the suggested refactorings. A survey of 7,758 React reposito-
ries showed that 92.1% of them exhibit at least one anti-pattern, and
careful experimental evaluation on 23 React projects revealed that
the suggested refactoring reduces the number of rendering opera-
tions by 33.3% on average while preserving application behavior in
all but one case. With a small increase in code complexity, we find
an average reduction in rendering time of 20.54%, and three case
studies reveal that the refactorings can greatly improve application
responsiveness as the number of components scales.