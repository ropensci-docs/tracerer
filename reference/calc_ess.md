# Calculates the Effective Sample Size

Calculates the Effective Sample Size

## Usage

``` r
calc_ess(trace, sample_interval)
```

## Arguments

- trace:

  the values without burn-in

- sample_interval:

  the interval in timesteps between samples

## Value

the effective sample size

## See also

Java code can be found here:
<https://github.com/CompEvol/beast2/blob/9f040ed0357c4b946ea276a481a4c654ad4fff36/src/beast/core/util/ESS.java#L161>
\# nolint URLs can be long

## Author

The original Java version of the algorithm was from Remco Bouckaert,
ported to R and adapted by Richèl J.C. Bilderbeek

## Examples

``` r
filename <- get_tracerer_path("beast2_example_output.log")
estimates <- parse_beast_tracelog_file(filename)
calc_ess(estimates$posterior, sample_interval = 1000)
#> [1] 11
```
