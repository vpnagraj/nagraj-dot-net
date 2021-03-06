+++
# Date this page was created.
date = "2018-04-02"

# Project title.
title = "LOLAweb"

# Project summary to display on homepage.
summary = "LOLAweb is a web server and interactive results viewer for enrichment of overlap between a query region set (a bed file) and a database of region sets. It provides an interactive result explorer to visualize the highest ranked enrichments from the database. You can access the web server at http://lolaweb.databio.org"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "lolaweb.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["sw-dev", "bioinformatics"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
# image = "brown.jpg"
# caption = "My caption :smile:"

+++

`LOLAweb` is an interactive application that implements functions from the LOLA package in a web interface via the [Shiny](https://shiny.rstudio.com/) framework.

The app is hosted and available for use at:

<http://lolaweb.databio.org>

To run the application locally, you'll need to first clone this repository:

```
git clone https://github.com/databio/LOLAweb.git
```

The app requires R to be installed, as well as several packages. From within R run the following to install the dependencies:

```
install.packages(c("ggplot2", "shiny", "DT", "shinyWidgets", "shinyjs", "sodium", "devtools", "shinyBS"))
devtools::install_github("databio/simpleCache")
devtools::install_github("databio/GenomicDistributions")

source("https://bioconductor.org/biocLite.R")
biocLite(c("LOLA", "GenomicRanges"))
```

You'll also need underlying data that is not available in this repository in order to establish the universes, example user sets and reference genome directories. Run the following from within the root of this folder to download the data and create the `universes/`, `userSets/`, `reference/` and `cache/` directories respectively:

```
# create universes dir
mkdir universes
mkdir userSets

# example universe and user set
curl http://cloud.databio.org.s3.amazonaws.com/vignettes/lola_vignette_data_150505.tgz | tar xvz

mv lola_vignette_data/activeDHS_universe.bed universes/.
mv lola_vignette_data/setB_100.bed userSets/.

rm -rf lola_vignette_data
```

```
# create reference dir
mkdir reference

# core
curl http://cloud.databio.org.s3.amazonaws.com/regiondb/LOLACoreCaches_170206.tgz | tar xvz
mv scratch/ns5bc/resources/regions/LOLACore reference/Core
rm -rf scratch

# extended
curl http://cloud.databio.org.s3.amazonaws.com/regiondb/LOLAExtCaches_170206.tgz | tar xvz
mv scratch/ns5bc/resources/regions/LOLAExt reference/Extended
rm -rf scratch
```

```
# create cache dir
mkdir cache
```
With all of the above installed you can now launch the app with `shiny::runApp()` from within R at the root of this directory.