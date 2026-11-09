---
title: "High-Performance Generation of Constrained Inputs"
collection: publications
permalink: /publication/2025-11-08-fandango-rs
excerpt: 'Language-based testing pairs grammars with semantic constraints, and solving those constraints has been slow. FANDANGO-RS compiles grammars into Rust types and uses better evolutionary algorithms, running 3-4 orders of magnitude faster than the prior state of the art and generating 401 valid C compiler inputs per minute.'
date: 2025-11-08
venue: 'arXiv (preprint)'
paperurl: 'https://arxiv.org/pdf/2511.05987'
citation: 'Addison Crump, Alexi Turcotte, José Antonio Zamudio Amaya, and Andreas Zeller. 2025. <i>High-Performance Generation of Constrained Inputs.</i> arXiv:2511.05987.'
---

Language-based testing combines context-free grammar definitions with semantic constraints over grammar elements to generate test inputs. By pairing context-free grammars with constraints, users have the expressiveness of unrestricted grammars while retaining simple structure. However, producing inputs in the presence of such constraints can be challenging. In past approaches, SMT solvers have been found to be very slow at finding string solutions; evolutionary algorithms are faster and more general, but current implementations still struggle with complex constraints that would be required for domains such as compiler testing. In this paper, we present a novel approach for evolutionary language-based testing that improves performance by 3-4 orders of magnitude over the current state of the art, reducing hours of generation and constraint solving time to seconds. We accomplish this by (1) carefully transforming grammar definitions into Rust types and trait implementations, ensuring that the compiler may near-maximally optimize arbitrary operations on arbitrary grammars; and (2) using better evolutionary algorithms that improve the ability of language-based testing to solve complex constraint systems. These performance and algorithmic improvements allow our prototype, FANDANGO-RS, to solve constraints that previous strategies simply cannot handle. We demonstrate this by a case study for a C subset, in which FANDANGO-RS is able to generate 401 diverse, complex, and valid test inputs for a C compiler per minute.
