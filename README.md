ANOVA and Contrasts in R
================

<!-- README.md is generated from README.Rmd. Please edit that file -->
*Last updated May 15, 2018*

Programme
=========

In a joint Berger-Kessler lab meeting (May 16, 2018), I will introduce and demonstrate how to conduct ANOVAs and compute contrasts (including interaction contrasts) in R using the afex and emmeans packages.

What you'll need to play along
==============================

-   These SPSS `.sav` files:
    -   [ChickWeight.sav](data/ChickWeight.sav)
    -   [anxiety.sav](data/anxiety.sav)
-   [R](https://cran.r-project.org/)
    -   Optional: [RStudio Desktop](https://www.rstudio.com/)
-   The following R packages:
    -   `haven` (for importing SPSS sav files)
    -   `tidyverse` (for data manipulation and ggplotting)
    -   `afex` (version 0.20-0 at least) (for running ANOVA)
    -   `emmeans` (for contrasts and simple slopes)
    -   `marginC` (my mini-package for setting contrasts with marginal weights).

Install these packages by running in the R command line:

``` r
install.packages(c("haven","afex","emmeans","tidyverse"))

# install.packages("devtools")
devtools::install_github("mattansb/marginC")
```

Reading Materials
=================

The following vignettes are the basis of the demo:
- [ANOVA with afex](https://github.com/singmann/afex/blob/master/vignettes/afex_anova_example.Rmd)
- [Contrasts](https://cran.r-project.org/web/packages/emmeans/vignettes/comparisons.html) and [interaction contrasts](https://cran.r-project.org/web/packages/emmeans/vignettes/interactions.html) with emmeans.

The Demo
========

The demo (code is available in the `code` folder) consists of two parts:

1.  Running Anovas and analyzing effects and interactions with contrasts (planned and post-hoc).
2.  Analyzing regression interactions.
