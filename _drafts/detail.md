---
layout: post
mathjax: true
title: A Tricky Detail from Convex Analysis
categories: linear algebra, analysis 
---

There's a detail that's quickly glossed over in a proof that the dimension of
the relative interior of a convex set is equal to the dimension of the set
itself:

If $x_0,\ldots,x_k$ is a set of $k+1$ affinely independent points, then if $y$
is such that there exist $a_0,\ldots,a_k \in \mathbb R$ with $y = \sum_{i=0}^k
a_ix_i$ and $\sum_{i=0}^k a_i$, then there exists $\delta > 0$ such that $\|y\|
< \delta$ implies $|a_i| < \frac 1 {k+1}$ for all $0 \le i \le k$. 

At first blush
