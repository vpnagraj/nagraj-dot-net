+++
# Date this page was created.
date = "2021-01-17"

# Project title.
title = "yawp"

# Project summary to display on homepage.
summary = "Home to miscellanea. Functions included are generic helpers for data manipulation, visualization, and analysis."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "code.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["sw-dev"]

badges = ["http://www.r-pkg.org/badges/version/yawp"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
# image = "headers/bubbles-wide.jpg"
# caption = "My caption :smile:"

+++

A collection of documented, tested, and packaged helper functions.

## Installation

``` r
devtools::install_github("vpnagraj/yawp", build_vignettes = TRUE)
```

Note that the install command above will install the package from GitHub
*and* build vignettes. If you would prefer not to build vignettes upon
install then set `build_vignettes = FALSE`, which is the default in
`devtools::install_github()`.

## Features

  - `betwixt()`: Find values between lower and upper bounds of a range
  - `bound()`: Bound a vector
  - `f1()`: Calculate F1 score
  - `first_char()`: Extract the first character from a string
  - `get_mode()`: Find the mode
  - `gg_zoom()`: Zoom in on a ggplot2 plot (*EXPERIMENTAL*)
  - `mav()`: Calculate moving average
  - `medf()`: Format median
  - `more()`: Add filler rows to a data frame
  - `propf()`: Calculate and format proportion
  - `read_repo()`: Read files directly from a GitHub repository
    (*EXPERIMENTAL*)
  - `summary_se()`: Calculate mean and standard error
  - `theme_mathbook()`: Custom “math book” ggplot2 theme

## Usage

The function documentation includes examples of usage, as do the package
vignettes:

``` r
browseVignettes(package = "yawp")
```

## Inspiration and Related Work

`yawp` is a utility package, and the functionality it provides is by no
means unique. In fact, some of the functions were directly inspired by
other tools. For example:

  - `betwixt()` builds on the concept originally implemented in the
    `between()` function in
    [dplyr](https://CRAN.R-project.org/package=dplyr) but adds a feature
    to ignore specific values
  - `summary_se()` re-implements `summarySE()` from [“The Cookbook for
    R”](http://www.cookbook-r.com/Manipulating_data/Summarizing_data/)
    with tidy eval syntax
  - The moving average functionality in `mav()` is available elsewhere,
    including for example in `slide()` from
    [slider](https://CRAN.R-project.org/package=slider)
  - While `f1()` calculates the F1 score, other available functions such
    as `f_meas()` from
    [yardstick](https://CRAN.R-project.org/package=yardstick) may
    accommodate more generic applications (i.e. applying weights to
    precision and recall)