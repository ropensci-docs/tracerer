# Parses a BEAST2 state `.xml.state` output file to get only the operators acceptances

Parses a BEAST2 state `.xml.state` output file to get only the operators
acceptances

## Usage

``` r
parse_beast_state_operators(
  state_filename = get_tracerer_path("beast2_example_output.xml.state"),
  filename = "deprecated"
)
```

## Arguments

- state_filename:

  name of the BEAST2 state `.xml.state` output file

- filename:

  deprecated name of the BEAST2 .xml.state output file, use
  `state_filename` instead

## Value

data frame with all the operators' success rates

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
parse_beast_state_operators(
  state_filename = get_tracerer_path("beast2_example_output.xml.state")
)
#>            operator    p accept reject acceptFC rejectFC rejectIv rejectOp
#> 1      treeScaler.t 0.50    184    186        0        0        0        0
#> 2  treeRootScaler.t 0.50    144    224        0        0       63       63
#> 3 UniformOperator.t  NaN   2219   1667        0        0        0        0
#> 4    SubtreeSlide.t 1.00    409   1442        0        0      690      690
#> 5          narrow.t  NaN    962    972        0        0        0        0
#> 6            wide.t  NaN     50    349        0        0      236      236
#> 7   WilsonBalding.t  NaN     31    365        0        0      230      230
#> 8 BirthRateScaler.t 0.75    347     73        0        0        0        0
#> 9 DeathRateScaler.t 0.75    329     48        0        0        3        3
```
