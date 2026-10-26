# Calculates the Effective Sample Sizes from a parsed BEAST2 log file

Calculates the Effective Sample Sizes from a parsed BEAST2 log file

## Usage

``` r
calc_esses(traces, sample_interval)
```

## Arguments

- traces:

  a dataframe with traces with removed burn-in

- sample_interval:

  the interval in timesteps between samples

## Value

the effective sample sizes

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# Parse an example log file
estimates <- parse_beast_tracelog_file(
  get_tracerer_path("beast2_example_output.log")
)

# Calculate the effective sample sizes of all parameter estimates
calc_esses(estimates, sample_interval = 1000)
#>   posterior likelihood prior treeLikelihood TreeHeight BirthDeath birthRate2
#> 1        11         11    11             11          8         11         11
#>   relativeDeathRate2
#> 1                  7
```
