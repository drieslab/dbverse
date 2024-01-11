
<!-- README.md is generated from README.Rmd. Please edit that file -->

# dbverse

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
<!-- badges: end -->

The `dbverse` is a set of open-source and composable packages for
larger-than-memory data analysis. The `dbverse` provides *object
relational mappings* for common data objects, including sparse and dense
matrices, spatial geometries, and others, and is powered by
[DuckDB](https://duckdb.org/).

The goal of `dbverse` is to enable users to analyze larger-than-memory
data objects using familiar coding syntax and methods provided by
existing in-memory packages. Please visit the
[**packages**](https://drieslab.github.io/dbverse/packages/) page for
details about each `dbverse` package.

Note: the `dbverse` is currently under active development.

## Installation

You can install the development version of `dbverse` like so:

``` r
# install.packages("pak", repos = sprintf("https://r-lib.github.io/p/pak/stable/%s/%s/%s", .Platform$pkgType, R.Version()$os, R.Version()$arch))
pak::pak("drieslab/dbverse")
```
