# Save the BEAST2 trees as a BEAST2 `.log` file There will be some differences: a BEAST2 `.log` file also saves the model as comments and formats the numbers in a way non-standard to R

Save the BEAST2 trees as a BEAST2 `.log` file There will be some
differences: a BEAST2 `.log` file also saves the model as comments and
formats the numbers in a way non-standard to R

## Usage

``` r
save_beast_trees(trees, filename)
```

## Arguments

- trees:

  BEAST2 posterior trees, of type `ape::multiPhylo`

- filename:

  name of the `.trees` file to save to

## Value

nothing

## See also

Use
[`parse_beast_log`](https://docs.ropensci.org/tracerer/reference/parse_beast_log.md)
to read a BEAST2 `.log` file

## Author

Richèl J.C. Bilderbeek
