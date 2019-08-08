Assignment\_1
================
Alex, Daniel and Micah
8/8/2019

1.  Load the Data.

<!-- end list -->

``` r
library(data.table)
d <- fread('../data/data.csv')
```

2.  Calculate a mean of `value` grouped by `x`.

<!-- end list -->

``` r
res <- d[ , .(mean_value = mean(value)), by = .(x)]
```

3.  Print this result to the screen.

The average is:

``` r
res
```

    ##    x mean_value
    ## 1: 1        1.0
    ## 2: 0        0.5
