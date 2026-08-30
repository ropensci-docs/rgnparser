# Changelog

## rgnparser 0.3.0

CRAN release: 2023-12-12

#### NEW FEATURES

- Support was added for gnparser arguments `cultivar`, `capitalize`,
  `diaereses` ([\#31](https://github.com/ropensci/rgnparser/issues/31))

#### MISC

- The default number of threads was changed to 1
  ([\#32](https://github.com/ropensci/rgnparser/issues/32))

- Website links and badges fixed
  ([\#28](https://github.com/ropensci/rgnparser/issues/28),
  [\#30](https://github.com/ropensci/rgnparser/issues/30))

#### DEFUNCT

- [`install_gnparser()`](https://docs.ropensci.org/rgnparser/reference/install_gnparser.md)
  has been deprecated to stay in compliance with CRAN policies
  (“Packages should not write in the user’s home filespace, nor anywhere
  else on the file system apart from the R session’s temporary
  directory”)

#### BUG FIX

- A bug was fixed where the `ignore_tags` argument was not respected
  ([\#31](https://github.com/ropensci/rgnparser/issues/31))

## rgnparser 0.2.6

CRAN release: 2023-02-13

#### BUG FIX

[`install_gnparser()`](https://docs.ropensci.org/rgnparser/reference/install_gnparser.md)
now downloads the correct binary file depending on the system it
installs ‘gnparser’ on.

## rgnparser 0.2.0

CRAN release: 2021-01-25

#### NEW FEATURES

- A new gnparser version (v1) is out. In addition, gnparser has moved
  from Gitlab to Github; which also required changes to
  [`install_gnparser()`](https://docs.ropensci.org/rgnparser/reference/install_gnparser.md)
  because we download Go binaries from the gnparser source repository
  ([\#7](https://github.com/ropensci/rgnparser/issues/7))
- As part of new gnparser version, arguments have changed in
  [`gn_parse()`](https://docs.ropensci.org/rgnparser/reference/gn_parse.md)
  and
  [`gn_parse_tidy()`](https://docs.ropensci.org/rgnparser/reference/gn_parse_tidy.md):
  `format` has been removed. `batch_size` and `ignore_tags` were added
  to both functions, while `details` was added to
  [`gn_parse()`](https://docs.ropensci.org/rgnparser/reference/gn_parse.md)
  only. See docs for details.
  ([\#11](https://github.com/ropensci/rgnparser/issues/11))
- gnparser v1 or greater is now required
  ([\#10](https://github.com/ropensci/rgnparser/issues/10))

#### DEFUNCT

- [`gn_debug()`](https://docs.ropensci.org/rgnparser/reference/gn_debug.md)
  is now defunct. the gnparser command for this function was removed in
  gnparser v1 ([\#9](https://github.com/ropensci/rgnparser/issues/9))

#### BUG FIXES

- [`gn_version()`](https://docs.ropensci.org/rgnparser/reference/gn_version.md)
  was broken with the new gnparser version, fixed now
  ([\#8](https://github.com/ropensci/rgnparser/issues/8))

## rgnparser 0.1.0

CRAN release: 2020-11-05

#### NEW FEATURES

- First submission to CRAN.
