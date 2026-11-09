---
title: "Feature-Focused Test Generation"
collection: publications
permalink: /publication/2026-10-01-feature-focused
excerpt: 'Grammar-based test generators cover the whole input space, which gets in the way when you want to test one feature. This paper treats test generation as a configuration problem: it extracts a feature model from the input specification, lets the tester pick features, and slices the specification so that only those features vary.'
date: 2026-10-01
venue: 'ASE'
paperurl: 'https://dl.acm.org/doi/abs/10.1145/3832783.3837479'
citation: 'José Antonio Zamudio Amaya, Gaetano Sapia, Alexi Turcotte, David Benavides, Marcel Böhme, and Andreas Zeller. 2026. <i>Feature-Focused Test Generation.</i> In 41st IEEE/ACM International Conference on Automated Software Engineering (ASE). https://doi.org/10.1145/3832783.3837479'
---

Specification-based test generators use formal specifications of input languages to produce valid test inputs for complex systems. They can thus be used to cover the entire input space of the system under test. This broad generation capability, however, can become a problem when one wants to focus test generation on a particular subset of the input space, say, a feature whose implementation has recently changed or is particularly critical.

In this paper, we propose Feature-Focused Test Generation (FFTG), an approach that treats specification-based test generation as a configuration problem. FFTG is deeply rooted in the theories of feature-oriented software development, enabling testers to select and combine features while resolving feature interactions. From the input specification, FFTG first extracts a feature model that represents alternate and optional expansions as possible feature values. After the tester selects which features to focus upon, FFTG specializes the specification accordingly, yielding what we name a slice that generates inputs in which only the focused features vary: "Please generate PNG inputs that have a fixed 8-bit color depth and an Adam7 interlacing, yet explore arbitrary animations."

We implement FFTG in a prototype named Compás and evaluate it on ten real specifications. We find that Compás-generated slices (1) effectively focus test generation on specific features, preserving validity with 100% of generated inputs accepted by the parser; (2) exercise unique code locations associated with the targeted features and thus enable traceability of features; and (3) enable test suite minimization, with a small set of slices retaining the aggregate coverage of the full suite while requiring fewer tests. To the best of our knowledge, this is the first work to apply techniques from product line engineering to specification-based testing.
