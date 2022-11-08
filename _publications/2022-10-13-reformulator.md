---
title: "reformulator: Automated Refactoring of the N+1 Problem in Database-Backed Applications"
collection: publications
permalink: /publication/2022-10-13-reformulator
excerpt: 'Object-relational mappings allow programmers to write object-oriented-looking database code, but this code is prone to the N+1 problem. This paper describes an approach to automtically detect and repair these issues.'
date: 2022-10-13
venue: 'ASE'
paperurl: 'http://reallytg.github.io/files/papers/reformulator.pdf'
citation: 'Alexi Turcotte, Mark W. Aldrich, and Frank Tip. <i>reformulator: Automated Refactoring of the N+1 Problem in Database-Backed Applications</i>. In 37th IEEE/ACM International Conference on Automated Software Engineering (ASE). Rochester, MI, USA. ACM, New York, NY, USA. 12 pages.'
---

An Object-Relational Mapping (ORM) provides an object-oriented interface to a database and facilitates the development of database-backed applications. In an ORM, programmers do not need to write queries in a separate query language such as SQL, they instead write ordinary method calls that are mapped by the ORM to database queries. This added layer of abstraction hides the significant performance cost of database operations, and misuse of ORMs can lead to far more queries being generated than necessary. Of particular concern is the infamous “N+1 problem”, where an initial query yields N results that are used to issue N subsequent queries. This anti-pattern is prevalent in applications that use ORMs, as it is natural to iterate over collections in object-oriented languages. However, iterating over data that originates from a database and calling an ORM method in each iteration may result in suboptimal performance. In such cases, it is often possible to reduce the number of round-trips to the database by issuing a single, larger query that fetches all desired results at once.

We propose an approach for automatically refactoring applications that use ORMs to eliminate instances of the “N+1 problem”, which relies on static analysis to detect data flow between ORM API calls. We implement this approach in a tool called Reformulator, targeting the Sequelize ORM in JavaScript, and evaluate it on 8 JavaScript projects. We found 44 N+1 query pairs in these projects, and Reformulator refactored all of them successfully, resulting in improved performance (up to 7.67x) while preserving program behavior. Further experiments demonstrate that the relative performance improvements grew as the database size was increased (up to 38.58x), and that front-end page load times were improved.