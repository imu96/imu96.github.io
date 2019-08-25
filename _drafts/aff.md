---
layout: post
mathjax: true
title: Some Details Concerning Affine Combinations
categories: [linear algebra, convex analysis]
---

$\def\sb{_}$
 
# A Detail

In the book _Fundamentals of Convex Analysis_ by Hiriart-Urruty and Lemarechal
there are a few details that are quickly glossed over in the proof that the
dimension of the relative interior of a convex set is equal to the dimension of
the set itself:

If $x_0,\ldots,x_k$ is a set of $k+1$ affinely independent points, and if $y$
is such that there exist $a_0,\ldots,a_k \in \mathbb R$ with $y = \sum_{i=0}^k
a_ix_i$ and $\sum_{i=0}^k a_i = 0$, then there exists $\delta > 0$ such that
$\lVert y\rVert < \delta$ implies $|a_i| \le \frac 1 {k+1}$ for all $0 \le i \le k$. 

There is actually an easy proof for this- one that was pointed out to me by a
kind passerby. It goes as follows:

Note that mapping $\alpha = (\alpha_0 \;\ldots \;\alpha_n)$ to $y$ is linear,
and therefore continuous. Furthermore, since $x_0,\ldots,x_n$ are affinely
independent by assumption, the map from $\alpha$ to $y$ is injective. From this
it follows the map from $y$ to $\alpha$ is well-defined, linear, and
continuous.

Now let $\alpha$ be arbitrary subject to its $\mathcal {\ell}^2$-norm being
less than $\frac 1 {(k+1)^2}$. Clearly this implies the absolute value of each
of its components is less than $\frac 1 {k+1}$. However by the definition of
continuity there exists $\delta > 0$ such that $\| y - 0\| < \delta$ implies
$\|\alpha - 0\| < \frac 1 {(k+1)^2}$, completing the proof. 

# An Analytic Proof

Warning: This is less nice and uses more machinery, but hey. A proof is a
proof. 

Note that it suffices to show there does not exist a sequence
$\\{\alpha^n\\}_{n=1}^\infty$ where each member of the sequence has infinity norm
strictly larger that $1 / (k+1)$ such that for every $\varepsilon > 0$ there
exists $N$ such that $n > N$ implies $\lVert y^n \rVert < \varepsilon$. 

Without loss of generality there exists a subsequence $
\\{\alpha^{n_i}\\}_{i=1}^\infty $ such that $ \lVert \alpha^{n_i} \rVert \sb{
\infty}= \lvert \alpha^{n_i}_1 \rvert > \frac 1 {k+1} $. 

# An Even Smaller Detail

Somewhere near the proof the dimension of a convex set $X$ is defined as the
dimension of its affine hull, which in turn is defined as the largest set of
affinely independent vectors in the affine space. However it does not
immediately follow that there exists a set of affine vectors in $X$ of the same
size. Here is a proof this is indeed the case:

We begin by observing that a set of vectors $x_0,\ldots,x_k$ is affinely
dependent if and only if the vectors $x_1 - x_0,\ldots, x_k - x_0$ are linearly
dependent. 

Claim: If $X$ is a $k$ dimensional convex set, then there exist
$S:=\{x_0,\ldots,x_k\} \subset X$ such that $S$ is a set of affinely
independent vectors. 

Proof: We show the fact that aff $X$ contains $k+1$ affinely independent
vectors implies $X$ contains $k+1$ affinely independent vectors as well. Let
$T:=\{y_0,\ldots,y_k\}$ be a set of points residing in the affine hull of $X$,
and let $S:=\{x_0,\ldots,x_l\}$ be a set of affinely independent points in $X$
itself, with $l < k+1$. 

Lemma: If $T$ is in the affine hull of $S$, then $T$ is not affinely
independent. Suppose the hypothesis. Then for $0 \le i \le k, 1\le j \le l$
there exists $a_{ij}$ such that 

$$y_i = \Big(\sum_{j=1}^l a_{ij} (x_j - x_0) \Big) + x_0$$ 

By the first observation we made, we know that $T$ is affinely independent if
and only if $y_1 - y_0, \ldots, y_k - y_0$ is linearly independent. However the
latter vectors inhabit the $l$ dimensional space spanned by $x_1 - x_0, \ldots,
x_l - x_0$, so it is linearly dependent, from which it follows $T$ is affinely
dependent. 

The contrapositive of the above lemma says if $T$ is affinely independent, then
all of its elements do not lie in the affine span of $S$ i.e. there exists $0
\le i \le k$ such that $y_i$ is not an affine combination of the elements in
$S$. However since $y_i$ lies in the affine hull of $X$, there must exist
points $z_1,\ldots,z_m \in X$ such that $y_i$ is a affine combination of them. 

Now if there exists $z_p$ such that $z_p$ is not an affine combination of the
vectors in $X$, then $S \cup \{z_p\}$ is a larger set of affinely independent
vectors in $X$. However if all $z_i$'s can be expressed as affine combinations
of $S$, it is not hard to show the $y_i$'s are all an affine combination of the
vectors in $S$ as well, contradicting the affine independence of $T$. Hence
there must exist such $z_p$, and in this way we can find $k+1$ affinely
independent vectors in $X$. 
