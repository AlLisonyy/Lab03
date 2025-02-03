Lab 03 - Nobel laureates
================
Allison Li
01/29/25

### Load packages and data

``` r
library(tidyverse) 
```

``` r
nobel <- read_csv("data/nobel.csv")
```

### Exercise 1

``` r
print(nobel)
```

    ## # A tibble: 935 × 26
    ##       id firstname   surname  year category affiliation city  country born_date 
    ##    <dbl> <chr>       <chr>   <dbl> <chr>    <chr>       <chr> <chr>   <date>    
    ##  1     1 Wilhelm Co… Röntgen  1901 Physics  Munich Uni… Muni… Germany 1845-03-27
    ##  2     2 Hendrik A.  Lorentz  1902 Physics  Leiden Uni… Leid… Nether… 1853-07-18
    ##  3     3 Pieter      Zeeman   1902 Physics  Amsterdam … Amst… Nether… 1865-05-25
    ##  4     4 Henri       Becque…  1903 Physics  École Poly… Paris France  1852-12-15
    ##  5     5 Pierre      Curie    1903 Physics  École muni… Paris France  1859-05-15
    ##  6     6 Marie       Curie    1903 Physics  <NA>        <NA>  <NA>    1867-11-07
    ##  7     6 Marie       Curie    1911 Chemist… Sorbonne U… Paris France  1867-11-07
    ##  8     8 Lord        Raylei…  1904 Physics  Royal Inst… Lond… United… 1842-11-12
    ##  9     9 Philipp     Lenard   1905 Physics  Kiel Unive… Kiel  Germany 1862-06-07
    ## 10    10 J.J.        Thomson  1906 Physics  University… Camb… United… 1856-12-18
    ## # ℹ 925 more rows
    ## # ℹ 17 more variables: died_date <date>, gender <chr>, born_city <chr>,
    ## #   born_country <chr>, born_country_code <chr>, died_city <chr>,
    ## #   died_country <chr>, died_country_code <chr>, overall_motivation <chr>,
    ## #   share <dbl>, motivation <chr>, born_country_original <chr>,
    ## #   born_city_original <chr>, died_country_original <chr>,
    ## #   died_city_original <chr>, city_original <chr>, country_original <chr>

There are 935 observations and 26 variables in the dataset. Each row in
the nobel dataset represents a Nobel Prize winner. That row includes all
the information about the person, such as name, year of winning, and the
category of the prize in each column.

### Exercise 2 Create a new data frame called nobel_living that filters fo

``` r
filtered_data <- filter(nobel,  is.na(died_date), !is.na(country), gender != "org")
filtered_data
```

    ## # A tibble: 228 × 26
    ##       id firstname   surname  year category affiliation city  country born_date 
    ##    <dbl> <chr>       <chr>   <dbl> <chr>    <chr>       <chr> <chr>   <date>    
    ##  1    68 Chen Ning   Yang     1957 Physics  Institute … Prin… USA     1922-09-22
    ##  2    69 Tsung-Dao   Lee      1957 Physics  Columbia U… New … USA     1926-11-24
    ##  3    95 Leon N.     Cooper   1972 Physics  Brown Univ… Prov… USA     1930-02-28
    ##  4    97 Leo         Esaki    1973 Physics  IBM Thomas… York… USA     1925-03-12
    ##  5    98 Ivar        Giaever  1973 Physics  General El… Sche… USA     1929-04-05
    ##  6    99 Brian D.    Joseph…  1973 Physics  University… Camb… United… 1940-01-04
    ##  7   101 Antony      Hewish   1974 Physics  University… Camb… United… 1924-05-11
    ##  8   103 Ben R.      Mottel…  1975 Physics  Nordita     Cope… Denmark 1926-07-09
    ##  9   106 Samuel C.C. Ting     1976 Physics  Massachuse… Camb… USA     1936-01-27
    ## 10   107 Philip W.   Anders…  1977 Physics  Bell Telep… Murr… USA     1923-12-13
    ## # ℹ 218 more rows
    ## # ℹ 17 more variables: died_date <date>, gender <chr>, born_city <chr>,
    ## #   born_country <chr>, born_country_code <chr>, died_city <chr>,
    ## #   died_country <chr>, died_country_code <chr>, overall_motivation <chr>,
    ## #   share <dbl>, motivation <chr>, born_country_original <chr>,
    ## #   born_city_original <chr>, died_country_original <chr>,
    ## #   died_city_original <chr>, city_original <chr>, country_original <chr>

there are 228 observations.

### Exercise 3

Remove this text, and add your answer for Exercise 1 here. Add code
chunks as needed. Don’t forget to label your code chunk. Do not use
spaces in code chunk labels.

### Exercise 4

…

### Exercise 5

…

### Exercise 6

…
