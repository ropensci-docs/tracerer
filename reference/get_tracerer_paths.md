# Get the full paths of files in the `inst/extdata` folder

Get the full paths of files in the `inst/extdata` folder

## Usage

``` r
get_tracerer_paths(filenames)
```

## Arguments

- filenames:

  the files' names, without the path

## Value

the filenames' full paths

## See also

for one file, use
[`get_tracerer_path`](https://docs.ropensci.org/tracerer/reference/get_tracerer_path.md)

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
get_tracerer_paths(
  c(
    "beast2_example_output.log",
    "beast2_example_output.trees",
    "beast2_example_output.xml",
    "beast2_example_output.xml.state"
  )
)
#> [1] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.log"      
#> [2] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.trees"    
#> [3] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.xml"      
#> [4] "/github/home/R/x86_64-pc-linux-gnu-library/4.6/tracerer/extdata/beast2_example_output.xml.state"
```
