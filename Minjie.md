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
janitor::clean_names() %>% view()
```

    ## Parsed with column specification:
    ## cols(
    ##   .default = col_double(),
    ##   `Week Ending` = col_character(),
    ##   `Provider Name` = col_character(),
    ##   `Submitted Data` = col_character(),
    ##   `Shortage of Nursing Staff` = col_character(),
    ##   `Shortage of Clinical Staff` = col_character(),
    ##   `Shortage of Aides` = col_character(),
    ##   `Shortage of Other Staff` = col_character(),
    ##   `One-Week Supply of N95 Masks` = col_character(),
    ##   `One-Week Supply of Surgical Masks` = col_character(),
    ##   `One-Week Supply of Eye Protection` = col_character(),
    ##   `One-Week Supply of Gowns` = col_character(),
    ##   `One-Week Supply of Gloves` = col_character(),
    ##   `One-Week Supply of Hand Sanitizer` = col_character(),
    ##   `Ventilator Dependent Unit` = col_character(),
    ##   `One-Week Supply of Ventilator Supplies` = col_character(),
    ##   County = col_character()
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
