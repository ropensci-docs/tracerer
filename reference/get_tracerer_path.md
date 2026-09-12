# Get the full path of a file in the `inst/extdata` folder

Get the full path of a file in the `inst/extdata` folder

## Usage

``` r
get_tracerer_path(filename)
```

## Arguments

- filename:

  the file's name, without the path

## Value

the full path to the filename

## See also

for more files, use
[`get_tracerer_paths`](https://docs.ropensci.org/tracerer/reference/get_tracerer_paths.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
get_tracerer_path("beast2_example_output.log")
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.log"
get_tracerer_path("beast2_example_output.trees")
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.trees"
get_tracerer_path("beast2_example_output.xml")
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.xml"
get_tracerer_path("beast2_example_output.xml.state")
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.xml.state"
```
