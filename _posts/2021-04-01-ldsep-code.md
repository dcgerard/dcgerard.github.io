---
title: Polyploid LD Estimation
category: code
layout: default
description: Estimate linkage disequilibrium in polyploids.
---

# ldsep: Linkage Disequilibrium Shrinkage Estimation for Polyploids

I posted a package to [CRAN](https://cran.r-project.org/package=ldsep)
to estimate haplotypic or composite pairwise linkage disequilibrium
(LD) in polyploids, using either genotypes or genotype
likelihoods. Support is provided to estimate the popular measures of
LD: the LD coefficient *D*, the standardized LD coefficient *D*′, and
the Pearson correlation coefficient *r*. All estimates are returned
with corresponding standard errors. These estimates and standard
errors can then be used for shrinkage estimation. The methods are
described in Gerard (2021a) and Gerard (2021b).

The main functions are:

-   `ldfast()`: Fast, moment-based approach to estimate pairwise LD in
    the presence of genotype uncertainty.
	
-   `ldest()`: Estimates pairwise LD via maximum likelihood.

-   `mldest()`: Iteratively apply `ldest()` across many pairs of SNPs.

-   `sldest()`: Iteratively apply `ldest()` along a sliding window of
    fixed length.
	
-   `plot.lddf()`: Plot method for the output of `mldest()` and
    `sldest()`.
	
-   `format_lddf()`: Format the output of `mldest()` and `sldest()` into
    a matrix.
	
-   `ldshrink()`: Shrink correlation estimates using adaptive shrinkage
    (Stephens, 2017; Dey and Stephens, 2018).

## Installation

You can install the released version of ldsep from
[CRAN](https://cran.r-project.org/package=ldsep) with:

``` r
install.packages("ldsep")
```

And the development version from
[GitHub](https://github.com/dcgerard/ldsep) with:

``` r
# install.packages("devtools")
devtools::install_github("dcgerard/ldsep")
```

## Citation

To cite `ldsep` in publications use:

> Gerard D (2021). "Pairwise Linkage Disequilibrium Estimation for
> Polyploids." *Molecular Ecology Resources*, *Accepted Author
> Manuscript*.
> [doi:10.1111/1755-0998.13349](https://doi.org/10.1111/1755-0998.13349).

A BibTeX entry for LaTeX users is

``` tex
@Article{,
  title = {Pairwise Linkage Disequilibrium Estimation for Polyploids},
  author = {David Gerard},
  journal = {Molecular Ecology Resources},
  year = {2021},
  doi = {10.1111/1755-0998.13349},
  volume = {Accepted Author Manuscript},
}
```

If you use `ldfast()`, please cite:

> Gerard D (2021). "Scalable Bias-corrected Linkage Disequilibrium
> Estimation Under Genotype Uncertainty." *bioRxiv*.
> [doi:10.1101/2021.02.08.430270](https://doi.org/10.1101/2021.02.08.430270).

A BibTeX entry for LaTeX users is

``` tex
@Article{,
  title = {Scalable Bias-corrected Linkage Disequilibrium Estimation Under Genotype Uncertainty},
  author = {David Gerard},
  journal = {bioRxiv},
  year = {2021},
  doi = {10.1101/2021.02.08.430270},
}
```

## References

-   Dey, Kushal K., and Matthew Stephens. "CorShrink: Empirical Bayes
    shrinkage estimation of correlations, with applications." *bioRxiv*
    (2018): 368316. [doi:10.1101/368316](https://doi.org/10.1101/368316)

-   Gerard, David. "Pairwise Linkage Disequilibrium Estimation for
    Polyploids." *Molecular Ecology Resources*. Accepted Author
    Manuscript. (2021a)
    [doi:10.1111/1755-0998.13349](https://doi.org/10.1111/1755-0998.13349)

-   Gerard, David. "Scalable Bias-corrected Linkage Disequilibrium
    Estimation Under Genotype Uncertainty." *bioRxiv*. (2021b)
    [doi:10.1101/2021.02.08.430270](https://doi.org/10.1101/2021.02.08.430270)

-   Stephens, Matthew. "False discovery rates: a new deal."
    *Biostatistics* 18, no. 2 (2017): 275-294.
    [doi:10.1093/biostatistics/kxw041](https://doi.org/10.1093/biostatistics/kxw041)
