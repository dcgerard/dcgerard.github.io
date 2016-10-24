---
title: Equivariance
category: research
layout: default
description: A description of my dissertational work on optimal equivariant covariance estimation for tensor datasets.
---

For covariance estimation in the multilinear normal model, others have
explored maximum likelihood estimation \[Hoff, 2011, Ohlson et al.,
2013, Manceur and Dutilleul, 2013\], regularized likelihood methods
\[Allen, 2011, He et al., 2014\], or Bayesian methods with
semi-conjugate priors \[Hoff, 2011\]. But little work has been done on
the optimality properties of such estimators. The optimality of an
estimator is frequently defined in terms of statistical risk. Suppose,
for data *X*, we have an estimator *t*(*X*) of a parameter *θ*. Denote
the loss of using *t*(*X*) when the truth is *θ* as
*L*(*θ*, *t*(*X*)) ∈ ℝ<sup>+</sup>. The risk, then, is the expected loss
at *θ* with respect to the distribution of *X*,
*R*(*θ*, *t*)=*E*\[*L*(*θ*, *t*(*X*))|*θ*\].

We can gain some clues on finding optimal estimators, in terms of
statistical risk, from studying the history of covariance estimation in
classical multivariate statistics. It was first shown in James and Stein
\[1961\] that in the multivariate normal model the maximum likelihood
estimator (MLE) is not admissible (there exist estimators that beat the
MLE in terms of risk everywhere). Indeed, it is not even minimax, and
considerable reductions in risk can be made over a wide range of the
parameter space \[Lin and Perlman, 1985\]. The approach of James and
Stein \[1961\] was to use equivariance: For *X* ∈ ℝ<sup>*p* × *n*</sup>,
such that vec(*X*)∼*N*<sub>*p* × *n*</sub>(0, *I*<sub>*n*</sub> ⊗ *Σ*),
only consider estimators such that
\\(\\hat{\\Sigma}(AX) = A \\hat{\\Sigma}A^T\\) for all *A* lower triangular
with positive diagonal elements. If we restrict ourselves to this class
estimators, then it is possible to find a uniformly best estimator, and
this best estimator dominates the sample covariance matrix in terms of
risk.

Using the notions of equivariance, in
<a href="#gerard2015equivariant">Gerard and Hoff \[2015\]</a> we
extended the results of James and Stein \[1961\] to the multilinear
normal model. Unlike for the multivariate normal model, there is no
simple characterization for the class of equivariant estimators in the
multilinear normal model (beyond the definition of equivariance, of
course). So we had to develop a generalized Bayes procedure to find the
best equivariant estimator. This also required the derivation of a
novel, yet simple, class of distributions over the space of symmetric
and positive definite matrices which we called the "mirror-Wishart"
distribution. The form of the estimator depends on the loss function we
choose, but we developed a class of loss functions which are natural
extensions of Stein's loss from the vector case to the tensor case. The
best equivariant estimator using these "multiway Stein" losses have
simple characterizations in terms of the posterior expectations of the
component precision matrices. These estimators are also minimax. And
unlike the estimator in James and Stein \[1961\], where the reductions
in risk are modest, we observed risks as low as 60% that of the MLE,
depending on the dimension of the tensor. This is <i>uniform</i>
reduction over the whole parameter space.

A colleague once told me that equivariance is "what mathematicians do
when they do statistics", intending it as a pejorative statement on the
methodology, so I wish to discuss my use of it briefly. People have
intuitive arguments as to why equivariance is reasonable (some of which
I believe, some of which I certainly do not). However, if our goal is
just to find reasonable estimators that have good risk performance, then
equivariance is not a bad strategy. To me, there are three reasons why
equivariance is appealing. The first is one of convenience: In many
models, the statistical risk of any equivariant estimator is constant,
so finding a best equivariant estimator reduces down to comparing one
number per estimator, and we can often find a best equivariant
estimator. The second reason is that in any group invariant estimation
problem, the MLE is equivariant, so if we find a best equivariant
estimator, then we find one that dominates the MLE in terms of risk.
This is thus an automatic way of finding estimators that beat the MLE, a
popular estimator. The final reason is that under many groups, the best
equivariant estimator will be minimax, so we have a way of automatically
finding minimax estimators. I believe these are compelling reasons to
explore the use of equivariance in estimation.
