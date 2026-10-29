# gn_parse_tidy

extract names using gnparser into a tidy tibble

## Usage

``` r
gn_parse_tidy(
  x,
  threads = 1,
  batch_size = NULL,
  cultivar = FALSE,
  capitalize = FALSE,
  diaereses = FALSE,
  ignore_tags = FALSE
)
```

## Arguments

- x:

  (character) vector of scientific names. required

- threads:

  (integer/numeric) number of threads to run for parallel processing.
  Setting to `NULL` will use all threads available. default: `1`

- batch_size:

  (integer/numeric) maximum number of names in a batch send for
  processing. default: `NULL`

- cultivar:

  (logical) adds support for botanical cultivars like
  `Sarracenia flava 'Maxima'` and graft-chimaeras like
  `+ Crataegomespilus`. default: `FALSE`

- capitalize:

  (logical) capitalizes the first letter of name-strings. default:
  `FALSE`

- diaereses:

  (logical) preserves diaereses within names, e.g.
  `Leptochloöpsis virgata`. The stemmed canonical name will be generated
  without diaereses. default: `FALSE`

- ignore_tags:

  (logical) ignore HTML entities and tags when parsing. default: `FALSE`

## Value

a data.frame

## Details

This function focuses on a data.frame result that's easy to munge
downstream - note that this function does not do additional details as
does
[`gn_parse()`](https://docs.ropensci.org/rgnparser/reference/gn_parse.md).

## Examples

``` r
trys <- function(x) try(x, silent=TRUE)
if (interactive()) {
x <- c("Quadrella steyermarkii (Standl.) Iltis & Cornejo",
  "Parus major Linnaeus, 1788", "Helianthus annuus var. texanus")
trys(gn_parse_tidy(x))
}
```
