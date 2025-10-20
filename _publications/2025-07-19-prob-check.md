---
title: "Expressing and Checking Statistical Assumptions"
collection: publications
permalink: /publication/2025-07-19-prob-check
excerpt: 'Statistics is tricky business, and programs meant to perform statistics do not give analysts feedback when they make mistakes. In this paper, we explore how data that does not appear to be compliant w.r.t. assumptions made by statistical methods affects the outcome of statistical tests, and propose an approach to automatically deliver feedback to analysts when such assumptions appear to be violated. <b>This paper received an ACM SIGSOFT Distinguished Paper Award!</b>'
date: 2025-07-19
venue: 'FSE'
paperurl: 'http://reallytg.github.io/files/papers/prob_check.pdf'
citation: 'Alexi Turcotte and Zheyuan Wu. 2025. <i>Expressing and Checking Statistical Assumptions.</i> Proc. ACM Softw. Eng. 2, FSE, Article FSE121 (July 2025), 24 pages. https://doi.org/10.1145/3729391'
---

Literate programming environments like Jupyter and R Markdown notebooks, coupled with easy-to-use languages like Python and R, put a plethora of statistical methods right at a data analyst’s fingertips. But are these methods being used correctly? Statistical methods make statistical assumptions about samples being analyzed, and in many cases produce reasonable looking results even if assumptions are not met.

We propose an approach that allows library developers to annotate functions with statistical assumptions, phrases them as hypotheses about the data, and inserts hypothesis tests investigating the likelihood that the assumption is met; this way, analysts using these functions will have their data checked automatically. We implement this approach in two tools: prob-check-py for Python, and prob-check-r for R, and to evaluate them we identify common hypothesis testing and statistical modeling functions, annotate them with the relevant statistical assumptions, and run 128 Kaggle notebooks that use those methods to identify misuses. Our investigation reveals statistically significant evidence against assumptions in 84.38% of surveyed notebooks, and in 53.36% of calls to annotated functions. In the case of hypothesis tests, had an equivalent test that did not make these assumptions been chosen, a different conclusion would have been drawn in 11.51% of cases.