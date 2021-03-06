<!-- README.md is generated from README.Rmd. Please edit that file -->
OpenCaseStudies
===============

[![Build
Status](https://travis-ci.org/opencasestudies/ocs-bp-co2-emissions.svg?branch=master)](https://travis-ci.org/opencasestudies/ocs-bp-co2-emissions)

### Disclaimer

The purpose of the [Open Case
Studies](https://opencasestudies.github.io) project is **to demonstrate
the use of various data science methods, tools, and software in the
context of messy, real-world data**. A given case study does not cover
all aspects of the research process, is not claiming to be the most
appropriate way to analyze a given dataset, and should not be used in
the context of making policy decisions without external consultation
from scientific experts.

### License

This case study is part of the
[OpenCaseStudies](https://opencasestudies.github.io) project. This work
is licensed under the Creative Commons Attribution-NonCommercial 3.0
([CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/us/))
United States License.

### Citation

To cite this case study:

Wright, Carrie, and Ontiveros, Michael and Jager, Leah and Taub,
Margaret and Hicks, Stephanie. (2020).
<a href="https://github.com/opencasestudies/ocs-bp-co2-emissions" class="uri">https://github.com/opencasestudies/ocs-bp-co2-emissions</a>.
Exploring CO2 emissions across time (Version v1.0.0).

### Acknowledgements

We would like to acknowledge [Megan
Latshaw](https://www.jhsph.edu/faculty/directory/profile/1708/megan-weil-latshaw)
for assisting in framing the major direction of the case study.

We would also like to acknowledge the [Bloomberg American Health
Initiative](https://americanhealth.jhu.edu/) for funding this work.

### Title

Exploring CO2 emissions across time

### Motivation

C02 emissions have been on the rise for many countries. CO2 emissions
trap heat in the atmosphere which can lead to increased global
temperatures which can cause vast influences on the health of people and
our planet. In this case study we explore national differences in CO2
emissions overtime. We evaluate the relationship between CO2 emissions
and average annual temperatures in the US. And we also examine the
relationship between emissions and natural disasters, as well as other
factors that may influence, be influenced by CO2 emissions.

### Motivating questions

1.  How have global CO2 emission rates changed over time? In particular
    for the US, and how does the US compare to other countries?
2.  Are CO2 emissions in the US, global temperatures, and natural
    disaster rates in the US associated?

### Data

In this case study we will be using data related to CO2 emissions, as
well as other data that may influence, be influenced or relate to CO2
emissions.

This case study uses data from
<a href="https://www.gapminder.org/data/" target="_blank">Gapminder</a>
that was originally obtained from the
<a href="https://www.worldbank.org/en/what-we-do" target="_blank">World Bank</a>.

In addition, we will use some data that is specific to the United States
from the
<a href="https://www.noaa.gov/" target="_blank">National Oceanic and Atmospheric Administration (NOAA)</a>,
which is an agency that collects weather and climate data.

#### Learning Objectives

Data science skills:

1.  Importing data from various types of Excel files and CSV files
2.  Apply action verbs in `dplyr` for data wrangling
3.  How to pivot between “long” and “wide” datasets
4.  Joining together multiple datasets using `dplyr`
5.  How to create effective longitudinal data visualizations with
    `ggplot2`
6.  How to add text, color, and labels to `ggplot2` plots
7.  How to create faceted `ggplot2` plots

Statistical concepts and methods:

1.  Introduction to correlation coefficient as a summary statistic
2.  Relationship between correlation and linear regression
3.  Correlation is not causation

#### Data import

Data from several .xlsx files and a couple of .csv files were imported
using `readxl` and `readr` respectively.

#### Data wrangling

This case study particularly focuses on renaming variables, modifying
variables, creating new variables, and modifying the shape of the data
using fuctions from the `dplyr` package such as: `rename()`, `mutate()`,
`pivot_longer()`, and `pivot_wider()`.

This case study also covers combining data with `bind_rows()` and
`full_join()` of the `dplyr` package, including a comparison of the two
functions.

We also cover filtering with the`filter()` function of the `dplyr`
package, removing NA values with the `drop_na()` function of the `tidyr`
package, arrange data with the `arrange()` function of the `dplyr`
package, as well as grouping and summarizing data with the `group_by()`
and `summarize()` functions of the `dplyr` package.

#### Data Visualization

We include a thorough and introductory explanation of ggplot2 including
how to add color, facets and labels to plots.

### Analysis

In this case study we look at the correaltion between CO2 emissions and
annual average temperatures in the US. We also evaluate the assocation
between the two using a linear regression. We discuss the relationship
between correlation and linear regression and how we interpret the
findings.

### Other notes and resources

<a href="https://www.tidyverse.org/" target="_blank">Tidyverse</a>  
<a href="https://rstudio.com/resources/cheatsheets/" target="_blank">RStudio cheatsheets</a>  
<a href="https://www.mathsisfun.com/data/correlation.html" target="_blank">Introduction to correlation</a>  
<a href="https://rafalab.github.io/dsbook/regression.html#corr-coefl" target="_blank">Correlation coefficient</a>  
<a href="https://dfrieds.com/math/correlation-does-not-imply-causation.html" target="_blank">Correlation does not imply causation</a>  
<a href="https://rafalab.github.io/dsbook/regression.html" target="_blank">Regression</a>

#### For users

There is a [`Makefile`](Makefile) in this folder that allows you to type
`make` to knit the case study contained in the `index.Rmd` to
`index.html` and it will also knit the [`README.Rmd`](README.Rmd) to a
markdown file (`README.md`).

#### For instructors

Instructors can start at the data visualization section or the data
analysis section. However, if you choose to start at the data analysis
section, you will need to remove the code for the main plot.

#### Target audience

This case study is appropriate for those new to R programming and new to
statistics. It is also appropriate for more advanced R users who are new
to the Tidyverse.

#### Suggested homework

Ask students to create a plot with labels showing the countries with the
lowest CO2 emission levels.

Ask students to plot CO2 emissions and other variables (e.g. energy use)
on a scatter plot, calculate the Pearson’s correlation coefficient, and
discuss results.
