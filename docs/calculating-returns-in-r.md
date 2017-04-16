# Calculating Returns in R

Just the essentials for calculating simple and log returns in R when X is a time series of prices, with `R` representing simple returns and `r` representing log returns. See "[A Tale of Two Returns](http://www.portfolioprobe.com/2010/10/04/a-tale-of-two-returns/)" for much more detail on the subject, and "[Returns with negative net asset values](http://www.portfolioprobe.com/2012/07/30/returns-with-negative-net-asset-values/)" for why to use log returns.

### Calculating log returns

Using standard base functions:

```
r <- diff(log(X))
```

Using the `ROC` function from the `TTR` package:

```
r <- ROC(X)
```

### Conversion

Log return to simple return:

```
R <- exp(r) - 1
```

Simple return to log return:

```
r <- log(R + 1)
```
