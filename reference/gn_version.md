# gn_version

get gnparser version information

## Usage

``` r
gn_version()
```

## Value

named list, with `version` and `build`

## Examples

``` r
trys <- function(x) try(x, silent=TRUE)
if (interactive()) {
trys(gn_version())
}
```
