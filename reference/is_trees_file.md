# Measure if a file a valid BEAST2 `.trees` file

Measure if a file a valid BEAST2 `.trees` file

## Usage

``` r
is_trees_file(trees_filename, verbose = FALSE)
```

## Arguments

- trees_filename:

  name of a BEAST2 posterior `.trees` file, as can be read using
  [parse_beast_trees](https://docs.ropensci.org/tracerer/reference/parse_beast_trees.md)

- verbose:

  set to TRUE for more output

## Value

TRUE if `trees_filename` is a valid `.trees` file

## See also

Most of the work is done by
[read.nexus](https://rdrr.io/pkg/ape/man/read.nexus.html)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# TRUE
is_trees_file(get_tracerer_path("beast2_example_output.trees"))
#> [1] TRUE
is_trees_file(get_tracerer_path("unplottable_anthus_aco.trees"))
#> [1] TRUE
is_trees_file(get_tracerer_path("anthus_2_4_a.trees"))
#> [1] TRUE
is_trees_file(get_tracerer_path("anthus_2_4_b.trees"))
#> [1] TRUE
# FALSE
is_trees_file(get_tracerer_path("mcbette_issue_8.trees"))
#> [1] FALSE
```
