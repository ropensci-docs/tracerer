# Parses a BEAST2 .trees output file

Parses a BEAST2 .trees output file

## Usage

``` r
parse_beast_trees(filename)
```

## Arguments

- filename:

  name of the BEAST2 .trees output file

## Value

the phylogenies in the posterior

## See also

Use
[`save_beast_trees`](https://docs.ropensci.org/tracerer/reference/save_beast_trees.md)
to save the phylogenies to a `.trees` file. Use
[is_trees_file](https://docs.ropensci.org/tracerer/reference/is_trees_file.md)
with `verbose = TRUE` to find out why a file is invalid

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
trees_filename <- get_tracerer_path("beast2_example_output.trees")
parse_beast_trees(trees_filename)
#> 11 phylogenetic trees
```
