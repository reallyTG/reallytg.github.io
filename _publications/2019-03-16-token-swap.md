---
title: "Token Swapping on Trees"
collection: publications
permalink: /publication/2019-03-16-token-swap
excerpt: 'From the algorithms problem sessions at Waterloo; this paper presents some results about token swapping on a tree, i.e., sorting with a transposition tree.'
date: 2019-03-16
venue: 'DMTCS'
paperurl: 'http://reallytg.github.io/files/papers/arxiv19-token-swap.pdf'
citation: 'Ahmad Biniaz, Kshitij Jain, Anna Lubiw, Zuzana Masárová, Tillmann Miltzow, Debajyoti Mondal, Anurag Murty Naredla, Josef Tkadlec, Alexi Turcotte. 2019. Token Swapping on Trees. DMTCS, 37 pages.'
---

The input to the token swapping problem is a graph with vertices v1, v2, ..., vn, and n tokens with labels 1, 2, ..., n, one on each vertex. 
The goal is to get token i to vertex vi for all i = 1, 2, ..., n using a minimum number of swaps, where a swap exchanges the tokens on the endpoints of an edge. 
We present some results about token swapping on a tree, also known as “sorting with a transposition tree”:

1. An optimum swap sequence may need to perform a swap on a leaf vertex that has the correct token (a “happy leaf”), disproving a conjecture of Vaughan.

2. Any algorithm that fixes happy leaves—as all known approximation algorithms for the problem do—has approximation factor at least 4/3. 
Furthermore, the two best-known 2-approximation algorithms have approximation factor exactly 2.

3. A generalized problem—weighted coloured token swapping—is NP-complete on trees, even when they are restricted to be subdivided stars, but solvable in polynomial time on paths and stars. 
In this version, tokens and vertices have colours, and colours have weights. 
The goal is to get every token to a vertex of the same colour, and the cost of a swap is the sum of the weights of the two tokens involved.

