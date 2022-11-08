---
title: "Reasoning About FFIs Without Modelling the Foreign Language"
collection: publications
permalink: /publication/2019-07-15-reasoning-ffi
excerpt: 'This paper explores how to build a formal semantics for interactions with a foreign-function interface without explicitly modelling the foreign language.'
date: 2019-07-15
venue: 'ECOOP'
paperurl: 'http://reallytg.github.io/files/papers/ecoop19-preprint.pdf'
citation: 'Alexi Turcotte, Ellen Arteca, and Gregor Richards. 2019. Reasoning About Foreign Function Interfaces Without Modelling the Foreign Language. <i>European Conference on Object-Oriented Programming</i>, ECOOP, Article 16 (July 2019), 32 pages.'
---

Foreign function interfaces (FFIs) allow programs written in one language (called the host language) to call functions written in another language (called the guest language), and are widespread throughout modern programming languages, with C FFIs being the most prevalent. Unfortunately, reasoning about C FFIs can be very challenging, particularly when using traditional methods which necessitate a full model of the guest language in order to guarantee anything about the whole language. To address this, we propose a framework for defining whole language semantics of FFIs without needing to model the guest language, which makes reasoning about C FFIs feasible. We show that with such a semantics, one can guarantee some form of soundness of the overall language, as well as attribute errors in well-typed host language programs to the guest language. We also present an implementation of this scheme, Poseidon Lua, which shows a speedup over a traditional Lua C FFI.
