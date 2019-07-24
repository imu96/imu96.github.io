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
a_ix_i$ and $\sum_{i=0}^k a_i = 0$, then there exists $\delta > 0$ such that
$\|y\| < \delta$ implies $|a_i| < \frac 1 {k+1}$ for all $0 \le i \le k$. 

There is actually an easy proof for this- one that was pointed out to me by a
kind passerby. It goes as follows:

Note that mapping $\alpha = (\alpha_0 \;\ldots \;\alpha_n)$ to $y$ is linear,
and therefore continuous. Furthermore, since $x_0,\ldots,x_n$ are affinely
independent by assumption, the map from $\alpha$ to $y$ is injective. From this
it follows the map from $y$ to $\alpha$ is well-defined, linear, and
continuous.
