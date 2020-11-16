Minjie’s codes
================

setups

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.3.2     ✓ purrr   0.3.4
    ## ✓ tibble  3.0.3     ✓ dplyr   1.0.2
    ## ✓ tidyr   1.1.2     ✓ stringr 1.4.0
    ## ✓ readr   1.3.1     ✓ forcats 0.5.0

    ## ── Conflicts ────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
library(readxl)
library(patchwork)


knitr::opts_chunk$set(
  fig.width = 6,
  fig.asp = .6,
  out.width = "90%"
)
theme_set(theme_minimal() +  theme(legend.position = "bottom"))

options(
  ggplots2.continuous.color = "viridis",
  ggplots2.continuous.fill = "viridus"
)

scale_colour_discrete = scale_colour_viridis_d
scale_fill_discrete = scale_fill_viridis_d
```

data cleaning

``` r
nystate = read_csv("./data/nystate.csv") %>% 
janitor::clean_names() 
```

    ## Parsed with column specification:
    ## cols(
    ##   .default = col_character(),
    ##   `Federal Provider Number` = col_double(),
    ##   `Provider Zip Code` = col_double(),
    ##   `Residents Weekly Admissions COVID-19` = col_double(),
    ##   `Residents Total Admissions COVID-19` = col_double(),
    ##   `Residents Weekly Confirmed COVID-19` = col_double(),
    ##   `Residents Total Confirmed COVID-19` = col_double(),
    ##   `Residents Weekly Suspected COVID-19` = col_double(),
    ##   `Residents Total Suspected COVID-19` = col_double(),
    ##   `Residents Weekly All Deaths` = col_double(),
    ##   `Residents Total All Deaths` = col_double(),
    ##   `Residents Weekly COVID-19 Deaths` = col_double(),
    ##   `Residents Total COVID-19 Deaths` = col_double(),
    ##   `Number of All Beds` = col_double(),
    ##   `Total Number of Occupied Beds` = col_double(),
    ##   `COVID-19 Point-of-Care Tests Performed on Residents Since Last Report` = col_double(),
    ##   `COVID-19 Point-of-Care Tests Performed on Staff and/or Personnel Since Last Report` = col_double(),
    ##   `Staff Weekly Confirmed COVID-19` = col_double(),
    ##   `Staff Total Confirmed COVID-19` = col_double(),
    ##   `Staff Weekly Suspected COVID-19` = col_double(),
    ##   `Staff Total Suspected COVID-19` = col_double()
    ##   # ... with 7 more columns
    ## )

    ## See spec(...) for full column specifications.

    ## Warning: 46 parsing failures.
    ##   row                     col               expected actual                 file
    ## 14137 Federal Provider Number no trailing characters   A081 './data/nystate.csv'
    ## 14138 Federal Provider Number no trailing characters   A081 './data/nystate.csv'
    ## 14139 Federal Provider Number no trailing characters   A081 './data/nystate.csv'
    ## 14140 Federal Provider Number no trailing characters   A081 './data/nystate.csv'
    ## 14141 Federal Provider Number no trailing characters   A081 './data/nystate.csv'
    ## ..... ....................... ...................... ...... ....................
    ## See problems(...) for more details.
