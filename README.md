clock
=====



[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip)
[![Build Status](https://travis-ci.com/ropenscilabs/clock.svg?branch=master)](https://travis-ci.com/ropenscilabs/clock)

Time with mocking capability via [timefuzz][]

**BEWARE: VERY ALPHA**

Package API:

 - `Clock`
 - `clock_now`

## Installation


```r
remotes::install_github("ropenscilabs/clock")
```


```r
library("clock")
```

## usage


```r
Clock$new(2009)$time
#> [1] "2009-01-01 12:00:00 PST"
Clock$new(2009, 3, 13)$time
#> [1] "2009-03-13 12:00:00 PDT"
Clock$new(2009, 3, 13, 1, 4, 53)$time
#> [1] "2009-03-13 01:04:53 PDT"
```


```r
x <- Clock$new()
x$now()
#> [1] "2019-02-19 14:27:42 PST"
x$utc()
#> [1] "2019-02-19 22:27:42 UTC"
x$now("UTC")
#> [1] "2019-02-19 22:27:42 UTC"
```


```r
clock_now()
#> [1] "2019-02-19 14:27:42 PST"
clock_now("UTC")
#> [1] "2019-02-19 22:27:42 UTC"
```


## Meta

* Please [report any issues or bugs](https://github.com/ropenscilabs/clock/issues).
* License: MIT
* Get citation information for `clock` in R doing `citation(package = 'clock')`
* Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

[![rofooter](https://ropensci.org/public_images/github_footer.png)](https://ropensci.org)

[timefuzz]: https://github.com/ropenscilabs/timefuzz