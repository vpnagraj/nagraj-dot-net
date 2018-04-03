+++
# Date this page was created.
date = "2018-04-02"

# Project title.
title = "rrefine"

# Project summary to display on homepage.
summary = "'OpenRefine' (formerly 'Google Refine') is a popular, open source data cleaning software. This package enables users to programmatically trigger data transfer between R and 'OpenRefine'. Available functionality includes project import, export and deletion."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "bubbles.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["r-packages"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/bubbles-wide.jpg"
caption = "My caption :smile:"

+++

<a href="https://travis-ci.org/vpnagraj/rrefine">
<img src="https://travis-ci.org/vpnagraj/rrefine.svg?branch=master" alt="Travis CI Status"></img></a> [![CRAN Release](http://www.r-pkg.org/badges/version/rrefine)](https://cran.r-project.org/packages=rrefine) ![](http://cranlogs.r-pkg.org/badges/rrefine)


## Introduction

[*OpenRefine*](http://openrefine.org/) (formerly *Google Refine*) is a popular, open source data cleaning software. **rrefine** enables users to programmatically trigger data transfer between R and *OpenRefine*. Using the functions available in this package, you can import, export or delete a project in *OpenRefine* directly from R. There are [several client libraries for automating *OpenRefine* tasks via Python, nodeJS and Ruby](https://github.com/OpenRefine/OpenRefine/wiki/Documentation-For-Developers#known-client-libraries-for-refine). **rrefine** extends this functionality to R users.

## Installation

The latest version of **rrefine** is availabe on [Github](https://github.com/vpnagraj/rrefine) and can be installed via **devtools**:

```
# install.packages("devtools")
devtools::install_github("vpnagraj/rrefine")
library(rrefine)
```

**rrefine** is also available on [CRAN](https://cran.r-project.org/web/packages/rrefine/index.html):

```
install.packages("rrefine")
library(rrefine)
```
## Functions

The package includes the following functionality:

- `refine_upload()` (upload data to *OpenRefine* from R)
- `refine_export()` (export data to R from *OpenRefine*)
- `refine_delete()` (delete *OpenRefine* project)

Descriptions and examples of usage are available in the package [manual](https://cran.r-project.org/web/packages/rrefine/rrefine.pdf) and [vignette](https://cran.r-project.org/web/packages/rrefine/vignettes/rrefine-vignette.html).

## Issues

Feature requests, bug reports or other questions should be directed to the [issue queue](https://github.com/vpnagraj/rrefine/issues). 