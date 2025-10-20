---
title: "The Fault in our Stats"
collection: publications
permalink: /publication/2025-11-17-stat-lint
excerpt: 'As mentioned below, statistics is tricky, but there are many steps that analysts can take to ensure that their data complies with assumptions made by the methods they use. This paper presents an approach to statically detect such cases, and importantly, statically detect when analysts fail to check assumptions. This approach also catches data dredging!'
date: 2025-11-17
venue: 'ASE'
paperurl: 'http://reallytg.github.io/files/papers/ase25_statlint_final_final.pdf'
citation: 'Alexi Turcotte and Neev Nirav Mehta. 2025. <i>The Fault in our Stats.</i> In 40th IEEE/ACM International Conference on Automated Software Engineering (ASE). Rochester, MI, USA. ACM, New York, NY, USA., 13 pages. DOI to come.'
---

Data analysts need to be careful when they apply
statistical inference techniques to data, as misuse of statistical
inference methods can lead an analyst to draw the wrong
conclusions. They need to be careful because, in the general
case, misuse of statistics does not result in obvious problems;
the numbers returned often look reasonable, and programs with
misuses of statistics do not crash. In this work, we propose a
technique to quickly and statically check data science programs
for compliance with statistics best practice rules, including
checking all assumptions made by statistical methods, as well
as correcting for the multiple comparison problem, or “data
dredging”. This technique is predicated on a novel statistics
intermediate representation, called SIR, that encodes the details
most salient to statistics. We implement this technique in a tool
called STAT-LINT, the first statistics linter, and evaluate STAT-
LINT on 90 Python data science notebooks, finding that only 14
fully check all obligations, only two apply any correction for
multiple comparisons, none validate model residuals, and over
two thirds of obligations go unchecked.