homework-01
================
Chun Pong Brian Chan
9/23/2021

## R Markdown

``` r
library(tidyverse)
```

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.3.3     ✓ purrr   0.3.4
    ## ✓ tibble  3.1.0     ✓ dplyr   1.0.5
    ## ✓ tidyr   1.1.3     ✓ stringr 1.4.0
    ## ✓ readr   1.4.0     ✓ forcats 0.5.1

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
library(readr)
AK20 <- read_csv("../../data/AK20.txt")
```

    ## 
    ## ── Column specification ────────────────────────────────────────────────────────
    ## cols(
    ##   .default = col_double(),
    ##   STATE_CODE_001 = col_character(),
    ##   STRUCTURE_NUMBER_008 = col_character(),
    ##   ROUTE_NUMBER_005D = col_character(),
    ##   HIGHWAY_DISTRICT_002 = col_character(),
    ##   COUNTY_CODE_003 = col_character(),
    ##   PLACE_CODE_004 = col_character(),
    ##   FEATURES_DESC_006A = col_character(),
    ##   CRITICAL_FACILITY_006B = col_logical(),
    ##   FACILITY_CARRIED_007 = col_character(),
    ##   LOCATION_009 = col_character(),
    ##   LRS_INV_ROUTE_013A = col_character(),
    ##   LONG_017 = col_character(),
    ##   MAINTENANCE_021 = col_character(),
    ##   OWNER_022 = col_character(),
    ##   FUNCTIONAL_CLASS_026 = col_character(),
    ##   DESIGN_LOAD_031 = col_character(),
    ##   RAILINGS_036A = col_character(),
    ##   TRANSITIONS_036B = col_character(),
    ##   APPR_RAIL_036C = col_character(),
    ##   APPR_RAIL_END_036D = col_character()
    ##   # ... with 37 more columns
    ## )
    ## ℹ Use `spec()` for the full column specifications.

    ## Warning: 179 parsing failures.
    ##  row             col           expected actual                  file
    ## 1033 YEAR_OF_IMP_097 1/0/T/F/TRUE/FALSE   2019 '../../data/AK20.txt'
    ## 1034 YEAR_OF_IMP_097 1/0/T/F/TRUE/FALSE   2017 '../../data/AK20.txt'
    ## 1035 YEAR_OF_IMP_097 1/0/T/F/TRUE/FALSE   2017 '../../data/AK20.txt'
    ## 1036 YEAR_OF_IMP_097 1/0/T/F/TRUE/FALSE   2017 '../../data/AK20.txt'
    ## 1037 YEAR_OF_IMP_097 1/0/T/F/TRUE/FALSE   2017 '../../data/AK20.txt'
    ## .... ............... .................. ...... .....................
    ## See problems(...) for more details.

    ## # A tibble: 6 x 7
    ##   STATE_CODE_001 STRUCTURE_NUMBER… YEAR_BUILT_027 RAILINGS_036A TRANSITIONS_036B
    ##   <chr>          <chr>                      <dbl> <chr>         <chr>           
    ## 1 02             0176                        1998 0             0               
    ## 2 02             0177                        2015 1             1               
    ## 3 02             0178                        1973 1             1               
    ## 4 02             0179                        2011 0             0               
    ## 5 02             0180                        2004 0             0               
    ## 6 02             0181                        2011 0             0               
    ## # … with 2 more variables: APPR_RAIL_036C <chr>, LOCATION_009 <chr>
