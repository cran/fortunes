

<!-- README.md is generated from README.qmd via: quarto render README.qmd --to gfm -->

# R Fortunes

## Overview

The R package [fortunes](https://zeileis.codeberg.page/fortunes/)
provides a collection of quotations, mostly from the [R mailing
lists](https://www.R-project.org/mail.html) as well as some other
channels such as code, documentation, social media, etc. Along with the
quotations there is R code that can display a random quotation or search
for a specific one.

The package was inspired by the [Unix
fortune](https://en.wikipedia.org/wiki/Fortune_(Unix)) program that can
display random messages from a database of quotations, typically used at
the beginning or end of a session or when starting a terminal.

The R package was intended to provide some wisdom and comic relief when
working with R. However, as an increasing number of R community members
felt that many of the quotations were too snarky or even toxic, the
collection of quotations is essentially preserved “as is” and only very
rarely updated.

## Installation

The stable version of `fortunes` is available from
[CRAN](https://CRAN.R-project.org/package=fortunes):

``` r
install.packages("fortunes")
```

The latest development version can be installed from
[R-universe](https://zeileis.R-universe.dev/fortunes):

``` r
install.packages("fortunes", repos = "https://zeileis.R-universe.dev")
```

## License

The package is available under the [General Public License version
3](https://www.gnu.org/licenses/gpl-3.0.html) or [version
2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)

## Get started

The main function in the package is `fortune()`. By default it obtains a
random quotation from the package’s collection:

``` r
library("fortunes")
set.seed(403)
fortune()
## 
## Python users often ask if a solution is "pythonic". But I am not aware of R
## users having any special name like "R-thritic" and that may be a good thing.
##    -- Avi E. Gross
##       R-help (September 2024)
```

Alternatively, one can search for a specific string in the quotations.
In case of multiple matches one random match is displayed:

``` r
fortune("WTFM")
## 
## This is all documented in TFM. Those who WTFM don't want to have to WTFM again
## on the mailing list. RTFM.
##    -- Barry Rowlingson
##       R-help (October 2003)
```

Finally, the quotations are numbered (in the order in which they were
collected) and can be accessed with their number:

``` r
fortune(27)
## 
## As to whether you can do a Lilliefors test for several groups, that depends
## entirely on your ability to understand what the underlying question would be
## (see Adams D 1979).
##    -- Knut M. Wittkowski
##       R-help (February 2004)
```

See the documentation and the vignette for more details.
