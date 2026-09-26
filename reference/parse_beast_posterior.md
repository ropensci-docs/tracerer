# Parses BEAST2 output files to a posterior

Parses BEAST2 output files to a posterior

## Usage

``` r
parse_beast_posterior(
  trees_filenames,
  tracelog_filename,
  log_filename = "deprecated"
)
```

## Arguments

- trees_filenames:

  the names of one or more a BEAST2 posterior `.trees` file. Each
  `.trees` file can be read using
  [parse_beast_trees](https://docs.ropensci.org/tracerer/reference/parse_beast_trees.md)

- tracelog_filename:

  name of the BEAST2 tracelog `.log` output file, as can be read using
  [parse_beast_tracelog_file](https://docs.ropensci.org/tracerer/reference/parse_beast_tracelog_file.md)

- log_filename:

  deprecated name of the BEAST2 tracelog `.log` output file. Use
  `tracelog_filename` instead

## Value

a list with the following elements:  

- `estimates`: parameter estimates

- `[alignment_id]_trees`: the phylogenies in the BEAST2 posterior.
  `[alignment_id]` is the ID of the alignment.

## See also

Use
[`remove_burn_ins`](https://docs.ropensci.org/tracerer/reference/remove_burn_ins.md)
to remove the burn-ins from the posterior's estimates
(`posterior$estimates`)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
trees_filenames <- get_tracerer_path("beast2_example_output.trees")
tracelog_filename <- get_tracerer_path("beast2_example_output.log")
posterior <- parse_beast_posterior(
  trees_filenames = trees_filenames,
  tracelog_filename = tracelog_filename
)
```
