+++
# Date this page was created.
date = "2018-04-02"

# Project title.
title = "hei"

# Project summary to display on homepage.
summary = "Calculates Healthy Eating Index (HEI) scores for National Health and Nutrition Examination Survey (NHANES) data sets to facilitate analysis of demographic and dietary differences."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "code.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = []

badges = ["https://travis-ci.org/timfolsom/hei.svg?branch=master", "http://www.r-pkg.org/badges/version/hei", "https://codecov.io/gh/timfolsom/hei/branch/master/graph/badge.svg", 
"https://cranlogs.r-pkg.org/badges/hei",
"http://joss.theoj.org/papers/10.21105/joss.00417/status.svg"]
 

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = ""
caption = ""

+++

### Overview
___
The goal of **hei** is to calculate Healthy Eating Index (HEI) scores from National Health and Nutrition Examination Survey (NHANES) data for use in dietary analyses. The HEI is a dietary metric designed by the USDA and NCI to gauge adherence to the US Dietary Guidelines.

### Installation
___

**hei** is available on [CRAN](https://cran.r-project.org/package=hei), and can be installed as follows:

```
install.packages("hei")
```

To install the development version hosted on this repository, use the **devtools** package and the following:

```
# install.packages("devtools")
devtools::install_github("timfolsom/hei")
```
### Getting Started
___
```
library(hei)
```

The **hei** package contains one key function:

>`hei()` takes as its arguments three data sets: an FPED data set, a NHANES dietary data set, and an NHANES demographic data set, returning a HEI score for each individual in the NHANES study being analyzed.

**hei** also includes `get_fped()` `get_diet()` and `get_demo()` for retrieving data from the Food Patterns Equivalents Database (FPED) and the NHANES dietary and demographic databases, respectively. The FPED data sets (in the public domain) retrieved by `get_fped()` are built into the package and have been converted to .csv files from the SAS data format in which they were originally published by their creators. `get_diet()` and `get_demo()` require the R package `nhanesA` which is employed to retrieve NHANES data sets directly from the web.
### Related Work
___
**hei** is intended as a tool to aid in the analysis of NHANES data. It is important to be familiar with NHANES and its complex survey design as well as the FPED, which is derived from NHANES, before beginning any analyses involving the HEI.

* [NHANES survey methods and analytical guidelines](https://wwwn.cdc.gov/nchs/nhanes/analyticguidelines.aspx)

* [FPED methodology and user guides](https://www.ars.usda.gov/northeast-area/beltsville-md/beltsville-human-nutrition-research-center/food-surveys-research-group/docs/fped-methodology/)

### Contributing

**hei** is licensed under the [GNU General Public License Version 3](https://www.gnu.org/licenses/gpl-3.0.txt). Questions, feature requests and bug reports are welcome via the [issue queue](https://github.com/vpnagraj/hei/issues). The maintainer will review pull requests and incorporate contributions at his discretion.