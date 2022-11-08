---
title: "npm-filter: Automating the Mining of Dynamic Information from npm Packages"
collection: publications
permalink: /publication/2022-10-17-npm-filter
excerpt: 'This paper presents a tool for automatically mining dynamic information from npm packages, including transitive dependencies and the presence of a test suite.'
date: 2022-10-17
venue: 'MSR (Tool)'
paperurl: 'http://reallytg.github.io/files/papers/npm-filter.pdf'
citation: 'Ellen Arteca and Alexi Turcotte. 2022. <i>npm-filter: Automating the Mining of Dynamic Information from npm Packages</i>. In Proceedings of the 19th International Conference on Mining Software Repositories (MSR). Association for Computing Machinery, New York, NY, USA, 304–308.'
---

The static properties of code repositories, e.g., lines of code, dependents, dependencies, etc. can be readily scraped from code hosting platforms such as GitHub, and from package management systems such as npm for JavaScript; Although no less important, information related to the dynamic properties of programs, e.g., number of tests in a test suite that pass or fail, is less readily available. The ability to easily collect this dynamic information could be immensely useful to researchers conducting corpus analyses, as they could differentiate projects based on properties that can only be observed by running them.

In this paper, we present npm-filter, an automated tool that can download, install, build, test, and run custom user scripts over the source code of JavaScript projects available on npm, the most popular JavaScript package manager. We outline this tool, describe its implementation, and show that npm-filter has already been useful in developing evaluation suites for multiple JavaScript tools.