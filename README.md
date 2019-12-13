
# ggcorrplot

[![Build
Status](https://travis-ci.org/caijun/ggcorrplot.svg?branch=master)](https://travis-ci.org/caijun/ggcorrplot)

Implementation of corrplot using ggplot2

## Introduction

Reinventing wheels is not what I like doing.
[corrplot](https://CRAN.R-project.org/package=corrplot) is a great R
package, but I am really tired of customizing the appearance of
corrplot, e.g., the space between colorbar and its tick labels, space
around the plot that I don’t know how to remove when writing it to PDF
on my macOS, etc. This is most likely because I am more familiar with
the Grammar of Graphics implemented in ggplot2 than the base plotting
system in R. There are several R packages (e.g.,
[ggcorrplot](https://github.com/kassambara/ggcorrplot) developed by
Alboukadel Kassambara, [ggcorr](https://github.com/briatte/ggcorr)
developed by François Briatte) that can visualize a correlation matrix
into a corrplot using ggplot2; however, they are unable to visualize a
correlation matrix using mixed methods. My version of **ggcorrplot** has
implemented only a subset of features of corrplot to meet my urgent
needs. See examples in the **Getting started** section.

## Installation

Get the development version from github:

``` r
if (!requireNamespace("devtools")) install.packages("devtools")
devtools::install_github("caijun/ggcorrplot")
```

## Getting started

The `mtcars` dataset will be used for demonstrating the functionalities
of **ggcorrplot**.

``` r
library(ggcorrplot)

data(mtcars)
corr <- cor(mtcars)
p.mat <- cor.mtest(mtcars, conf.level = 0.95)

# visualize the correlation matrix
# --------------------------------
# method = "circle" (default)
ggcorrplot(corr)
```

## Contact

Bugs and feature requests can be filed to
<https://github.com/caijun/ggcorrplot/issues>. Pull requests are also
welcome.
