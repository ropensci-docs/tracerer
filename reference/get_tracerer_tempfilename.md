# Get a temporary filename

Get a temporary filename, similar to
[tempfile](https://rdrr.io/r/base/tempfile.html), except that it always
writes to a temporary folder named
[tracerer](https://docs.ropensci.org/tracerer/reference/tracerer-package.md).

## Usage

``` r
get_tracerer_tempfilename(pattern = "file", fileext = "")
```

## Arguments

- pattern:

  a non-empty character vector giving the initial part of the name.

- fileext:

  a non-empty character vector giving the file extension

## Value

name for a temporary file

## Note

this function is added to make sure no temporary cache files are left
undeleted
