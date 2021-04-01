---
title: RNA-seq Data Simulations
category: research
layout: default
description: Data-based simulations of RNA-seq.
---

A major issue with evaluating the large number of RNA-seq methods
available is that, in real data, the form and strength of unwanted
variation within these data is never known 
(see <a href="{{ site.url }}/research/2017/06/29/ruv.html">here</a> 
for motivation about unwanted variation). This creates issues with
benchmarking --- when researchers evaluate a method, they simulate
data only under the conditions that they assume (or minor deviations
from these assumptions), and so their performance on real data is
never accurately gauged. For my first solo-author publication (Gerard,
2020), I sought to create realistic simulation methods that accurately
capture the unknown structure of unwanted variation in RNA-seq
datasets. I did this by taking real RNA-seq data and adding known
signal to it. I proved that my method of adding signal is guaranteed
to work under a very flexible class of distributions on the RNA-seq
read-counts. These simulation techniques are all implemented in my
published software package,
[seqgendiff](https://cran.r-project.org/package=seqgendiff).

References
----------

Gerard, David. 2020. Data-based RNA-seq simulations by binomial thinning. *BMC Bioinformatics* 21(1). p. 206. [doi:10.1186/s12859-020-3450-9](https://doi.org/10.1186/s12859-020-3450-9).
