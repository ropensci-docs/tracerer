# Calculates the Effective Sample Sizes of one estimated variable's trace

Calculates the Effective Sample Sizes of one estimated variable's trace

## Usage

``` r
calc_summary_stats_trace(trace, sample_interval)
```

## Arguments

- trace:

  a numeric vector of values. Assumes the burn-in is removed.

- sample_interval:

  the interval in timesteps between samples

## Value

the effective sample sizes

## See also

Use
[`remove_burn_in`](https://docs.ropensci.org/tracerer/reference/remove_burn_in.md)
to remove the burn-in of a trace

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
estimates_all <- parse_beast_tracelog_file(
  get_tracerer_path("beast2_example_output.log")
)
estimates <- remove_burn_ins(estimates_all, burn_in_fraction = 0.1)

calc_summary_stats_trace(
  estimates$posterior,
  sample_interval = 1000
)
#>        mean stderr_mean    stdev variance    median mode geom_mean
#> 1 -70.58394   0.5044887 1.681629 2.827876 -69.87976  n/a       n/a
#>   hpd_interval_low hpd_interval_high  act ess
#> 1        -74.15268         -68.68523 1000  10
```
