# FRED Data

The Federal Reserve Bank of St. Louis’ [FRED](http://research.stlouisfed.org/fred2/) website provides quite a bit of current and historical economic data including 20 different [volatility](http://research.stlouisfed.org/fred2/release?rid=200&soid=47) indices from the Chicago Board Options Exchange (CBOE).

To download FRED data directly into R, use `fImport`’s `fredSeries` function and the Series ID, in this example "VIXCLS".

``` r
library(fImport)

vixcls <- fredSeries("VIXCLS", from = "1990-01-02")
trying URL 'http://research.stlouisfed.org/fred2/series/VIXCLS/downloaddata/VIXCLS.txt'
Content type 'text/plain; charset=UTF-8' length 103749 bytes (101 Kb)
opened URL
==================================================
downloaded 101 Kb

Read 5439 items
```
