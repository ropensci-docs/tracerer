# Documentation of general function arguments

This function does nothing. It is intended to inherit function argument
documentation.

## Usage

``` r
default_params_doc(
  log_filename,
  sample_interval,
  state_filename,
  trace,
  tracelog_filename,
  trees_filename,
  trees_filenames,
  verbose
)
```

## Arguments

- log_filename:

  deprecated name of the BEAST2 tracelog `.log` output file. Use
  `tracelog_filename` instead

- sample_interval:

  the interval in timesteps between samples

- state_filename:

  name of the BEAST2 state `.xml.state` output file

- trace:

  the values

- tracelog_filename:

  name of the BEAST2 tracelog `.log` output file, as can be read using
  [parse_beast_tracelog_file](https://docs.ropensci.org/tracerer/reference/parse_beast_tracelog_file.md)

- trees_filename:

  name of a BEAST2 posterior `.trees` file, as can be read using
  [parse_beast_trees](https://docs.ropensci.org/tracerer/reference/parse_beast_trees.md)

- trees_filenames:

  the names of one or more a BEAST2 posterior `.trees` file. Each
  `.trees` file can be read using
  [parse_beast_trees](https://docs.ropensci.org/tracerer/reference/parse_beast_trees.md)

- verbose:

  set to TRUE for more output

## Note

This is an internal function, so it should be marked with `@noRd`. This
is not done, as this will disallow all functions to find the
documentation parameters

## Author

Richèl J.C. Bilderbeek
