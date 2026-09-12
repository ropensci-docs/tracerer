# Count the number of trees in a `.trees` file

Count the number of trees in a `.trees` file

## Usage

``` r
count_trees_in_file(trees_filename)
```

## Arguments

- trees_filename:

  name of a BEAST2 posterior `.trees` file, as can be read using
  [parse_beast_trees](https://docs.ropensci.org/tracerer/reference/parse_beast_trees.md)

## Value

the number of trees

## See also

if the `.trees` file is invalid, use
[is_trees_file](https://docs.ropensci.org/tracerer/reference/is_trees_file.md)
with `verbose = TRUE` for the reason

## Author

Richèl J.C. Bilderbeek
