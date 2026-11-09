---
title: "Synthesizing Realistic Test Data without Breaking Privacy"
collection: publications
permalink: /publication/2026-03-23-private-data-gen
excerpt: 'Realistic test data often comes from real, private data. This workshop paper generates tabular data with a grammar-based fuzzer and uses a decision-tree discriminator to keep the samples it cannot tell apart from the original, iterating until the generated data looks real without copying it.'
date: 2026-03-23
venue: 'VERIFAI (Workshop)'
citation: 'Laura Plein, Alexi Turcotte, Arina Hallemans, and Andreas Zeller. 2026. <i>Synthesizing Realistic Test Data without Breaking Privacy.</i> In the VERIFAI Workshop.'
---

We describe a dataset with a grammar, generate samples from it with a fuzzer, and train a decision-tree classifier to tell generated samples apart from the original data. Samples the classifier takes for originals seed the next round of generation, and the discriminator is retrained each round on the newest data.
