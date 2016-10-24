---
title: Equivariant Estimation
category: research
layout: default
description: A description of my dissertational work on optimal equivariant covariance estimation for tensor datasets.
---

<p>For covariance estimation in the multilinear normal model, others have explored maximum likelihood estimation [Hoff, 2011, Ohlson et al., 2013, Manceur and Dutilleul, 2013], regularized likelihood methods [Allen, 2011, He et al., 2014], or Bayesian methods with semi-conjugate priors [Hoff, 2011]. But little work has been done on the optimality properties of such estimators. The optimality of an estimator is frequently defined in terms of statistical risk. Suppose, for data \(X\), we have an estimator \(t(X)\) of a parameter \(\theta\). Denote the loss of using \(t(X)\) when the truth is \(\theta\) as \(L(\theta,t(X)) \in \mathbb{R}^+\). The risk, then, is the expected loss at \(\theta\) with respect to the distribution of \(X\), \(R(\theta,t) = E[L(\theta,t(X))|\theta]\). </p>

<p>We can gain some clues on finding optimal estimators, in terms of statistical risk, from studying the history of covariance estimation in classical multivariate statistics. It was first shown in  James and Stein [1961] that in the multivariate normal model the maximum likelihood estimator (MLE) is not admissible (there exist estimators that beat the MLE in terms of risk everywhere). Indeed, it is not even minimax, and considerable reductions in risk can be made over a wide range of the parameter space [Lin and Perlman, 1985]. The approach of James and Stein [1961] was to use equivariance: For \(X \in \mathbb{R}^{p \times n}\), such that \(\text{vec}(X) \sim N_{p\times n}(0,I_n \otimes \Sigma)\), only consider estimators such that \(\hat{\Sigma}(AX) = A \hat{\Sigma}A^T\) for all \(A\) lower triangular with positive diagonal elements. If we restrict ourselves to this class estimators, then it is possible to find a uniformly best estimator, and this best estimator dominates the sample covariance matrix in terms of risk.</p>

<p>Using the notions of equivariance, in Gerard and Hoff [2015] we extended the results of James and Stein [1961] to the multilinear normal model. Unlike for the multivariate normal model, there is no simple characterization for the class of equivariant estimators in the multilinear normal model (beyond the definition of equivariance, of course). So we had to develop a generalized Bayes procedure to find the best equivariant estimator. This also required the derivation of a novel, yet simple, class of distributions over the space of symmetric and positive definite matrices which we called the "mirror-Wishart" distribution. The form of the estimator depends on the loss function we choose, but we developed a class of loss functions which are natural extensions of Stein's loss from the vector case to the tensor case. The best equivariant estimator using these "multiway Stein" losses have simple characterizations in terms of the posterior expectations of the component precision matrices. These estimators are also minimax. And unlike the estimator in  James and Stein [1961], where the reductions in risk are modest, we observed risks as low as \(60\%\) that of the MLE, depending on the dimension of the tensor. This is <i>uniform</i> reduction over the whole parameter space.</p>


<p>A colleague once told me that equivariance is "what mathematicians do when they do statistics", intending it as a pejorative statement on the methodology, so I wish to discuss my use of it briefly. People have intuitive arguments as to why equivariance is reasonable (some of which I believe, some of which I certainly do not). However, if our goal is just to find reasonable estimators that have good risk performance, then equivariance is not a bad strategy. To me, there are three reasons why equivariance is appealing. The first is one of convenience: In many models, the statistical risk of any equivariant estimator is constant, so finding a best equivariant estimator reduces down to comparing one number per estimator, and we can often find a best equivariant estimator. The second reason is that in any group invariant estimation problem, the MLE is equivariant, so if we find a best equivariant estimator, then we find one that dominates the MLE in terms of risk. This is thus an automatic way of finding estimators that beat the MLE, a popular estimator. The final reason is that under many groups, the best equivariant estimator will be minimax, so we have a way of automatically finding minimax estimators. I believe these are compelling reasons to explore the use of equivariance in estimation.</p>

<hr>

## References

- Genevera I. Allen. [Comment on article by Hoff](http://dx.doi.org/10.1214/11-BA606A) [mr2806238]. *Bayesian Anal.*, 6(2):197–201, 2011. ISSN 1936-0975. doi: 10.1214/11-BA606A.

- **David Gerard** and Peter Hoff. Equivariant minimax dominators of the MLE in the array normal model. *J. Multivariate Anal.*, 137:32–49, 2015. doi: 10.1016/j.jmva.2015.01.020. [[Link to JMVA]](http://www.sciencedirect.com/science/article/pii/S0047259X15000330) [[Link to arXiv]](http://arxiv.org/pdf/1408.0424.pdf)

- Shiyuan He, Jianxin Yin, Hongzhe Li, and Xing Wang. [Graphical model selection and estimation for high dimensional tensor data](http://dx.doi.org/10.1016/j.jmva.2014.03.007). *J. Multivariate Anal.*, 128:165–185, 2014. ISSN 0047-259X. doi: 10.1016/j.jmva.2014.03.007.

- Peter D. Hoff. [Separable covariance arrays via the Tucker product, with applications to multivariate relational data](http://dx.doi.org/10.1214/11-BA606). *Bayesian Anal.*, 6(2):179–196, 2011. ISSN 1936-0975. doi: 10.1214/11-BA606.

- W. James and Charles Stein. Estimation with quadratic loss. *In Proc. 4th Berkeley Sympos. Math. Statist. and Prob., Vol. I*, pages 361–379. Univ. California Press, Berkeley, Calif., 1961.

- Shang P. Lin and Michael D. Perlman. A Monte Carlo comparison of four estimators of a covariance matrix. *In Multivariate analysis VI* (Pittsburgh, Pa., 1983), pages 411–429. North-Holland, Amsterdam, 1985.

- Ameur M. Manceur and Pierre Dutilleul. [Maximum likelihood estimation for the tensor normal distribution: algorithm, minimum sample size, and empirical bias and dispersion](http://dx.doi.org/10.1016/j.cam.2012.09.017). *J. Comput. Appl. Math.*, 239:37–49, 2013. ISSN 0377-0427. doi: 10.1016/j.cam.2012.09.017.

- Martin Ohlson, M. Rauf Ahmad, and Dietrich von Rosen. [The multilinear normal distribution: introduction and some basic properties](http://dx.doi.org/10.1016/j.jmva.2011.05.015). *J. Multivariate Anal.*, 113:37–47, 2013. ISSN 0047-259X. doi: 10.1016/j.jmva.2011.05.015.