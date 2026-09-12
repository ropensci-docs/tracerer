# Determines if the input is a BEAST2 posterior

Determines if the input is a BEAST2 posterior

## Usage

``` r
is_posterior(x)
```

## Arguments

- x:

  the input

## Value

TRUE if the input contains all information of a BEAST2 posterior.
Returns FALSE otherwise.

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
trees_filename <- get_tracerer_path("beast2_example_output.trees")
tracelog_filename <- get_tracerer_path("beast2_example_output.log")
posterior <- parse_beast_posterior(
  trees_filename = trees_filename,
  tracelog_filename = tracelog_filename
)
is_posterior(posterior)
#> [1] TRUE
```
