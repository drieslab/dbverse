<!-- README.md is generated from README.Rmd. Please edit that file -->

# dbverse

<!-- badges: start -->
[![Lifecycle: experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

`dbverse` is a collection of open-source libraries for representing and
analyzing virtually any omic data in a fast and embeddable database
powered by DuckDB. On release, `dbverse` supports three core data types
commonly used in the omics field including *sequences* (e.g. bam/SAM,
fastq/fasta, and more), *geometries* (e.g. geojson, shp, and more), and
*counts* (e.g. sparse/dense matrices, data.frames).

The goals of `dbverse` are to:

1.  eliminate bottlenecks with analyzing large omic data (e.g. system
    memory constraints, limited access to complex and costly cloud
    computing infrastructure, etc.)
2.  enhance scientific reproducibility by providing a common format for
    representing and analyzing omics data
3.  enable researchers to perform multi-modal analyses in a variety of
    languages including SQL, python, R, and more through a common
    interface. On release, support for R and SQL are available.

`dbverse` was designed with a bottom-up approach, starting with three
core data sources commonly used in scientific computing:
counts/matrices, geometries, and biological sequences. The `dbverse`
core libraries can be used individually or together through this package
for multi-modal analysis. Please visit the **packages** page for
more details.

## Installation

You can install the development version of dbverse like so:

```{r, eval = FALSE}
# install.packages("pak", repos = sprintf("https://r-lib.github.io/p/pak/stable/%s/%s/%s", .Platform$pkgType, R.Version()$os, R.Version()$arch))
pak::pak("ed2uiz/dbverse")
```
