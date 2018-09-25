
[![Travis-CI Build Status](https://travis-ci.org/bautheac/BBGsymbols.svg?branch=master)](https://travis-ci.org/bautheac/BBGsymbols)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/bautheac/BBGsymbols?branch=master&svg=true)](https://ci.appveyor.com/project/bautheac/BBGsymbols)
[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)

# BBGsymbols

A collection of helper datasets for working with Bloomberg financial data in R.

## Installation

Install the development version from [github](https://github.com/bautheac/BBGsymbols/) with:

``` r
devtools::install_github(repo = "BBGsymbols", username = "bautheac")
```

## Example

Popular Bloomberg data field symbols for various financial instruments and corresponding data types.

``` r
library(BBGsymbols)
data(list = c("fields"), package = "BBGsymbols", envir = environment())
```
