---
title: RNA-seq Simulation
category: code
layout: default
description: Code for RNA-seq simulation.
---

# RNA-Seq Generation/Modification for Simulation

I posted a package to
[CRAN](https://cran.r-project.org/package=seqgendiff) that will take real
RNA-seq data (either single-cell or bulk) and alter it by adding
signal to it. This signal is in the form of a generalized linear model
with a log (base-2) link function under a Poisson / negative binomial
/ mixture of negative binomials distribution. The advantage of this
way of simulating data is that you can see how your method behaves
when the simulated data exhibit common (and annoying) features of real
data. This is without you having to specify these features *a
priori*. We call the way we add signal “binomial thinning”.

The main functions are:

- `select_counts()`: Subsample the columns and rows of a real RNA-seq
  count matrix. You would then feed this sub-matrix into one of the
  thinning functions below.
  
- `thin_diff()`: The function most users should be using for
  general-purpose binomial thinning. For the special applications of
  the two-group model or library/gene thinning, see the functions
  listed below.
  
- `thin_2group()`: The specific application of thinning in the two-group
  model.
  
- `thin_lib()`: The specific application of library size thinning.

- `thin_gene()`: The specific application of total gene expression
  thinning.
  
- `thin_all()`: The specific application of thinning all counts.

- `effective_cor()`: Returns an estimate of the actual correlation
  between the surrogate variables and a user-specified design matrix.
  
- `ThinDataToSummarizedExperiment()`: Converts a `ThinData` object to a
  `SummarizedExperiment` object.
  
- `ThinDataToDESeqDataSet()`: Converts a `ThinData` object to a
  `DESeqDataSet` object.

# Installation

To install from CRAN, run the following code in R:

``` r
install.packages("seqgendiff")
```

To install the latest version of seqgendiff, run the following code in
R:

``` r
install.packages("devtools")
devtools::install_github("dcgerard/seqgendiff")
```

To get started, check out the vignettes by running the following in R:

``` r
library(seqgendiff)
browseVignettes(package = "seqgendiff")
```

Or you can check out the vignettes I post online:
<https://dcgerard.github.io/seqgendiff/>.

# Citation

If you use this package, please cite:

> Gerard D (2020). "Data-based RNA-seq simulations by binomial
> thinning." *BMC Bioinformatics*. 21(1), 206. doi:
> [10.1186/s12859-020-3450-9](https://doi.org/10.1186/s12859-020-3450-9).

A BibTeX entry for LaTeX users is

``` tex
@article{gerard2020data,
    author = {Gerard, David},
    title = {Data-based {RNA}-seq simulations by binomial thinning},
    year = {2020},
    volume={21},
    number={1},
    pages={206},
    doi = {10.1186/s12859-020-3450-9},
    publisher = {BioMed Central Ltd},
    journal = {BMC Bioinformatics}
}
```
