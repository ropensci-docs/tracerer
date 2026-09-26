# Calculates the Effective Sample Sizes of the traces of multiple estimated variables

Calculates the Effective Sample Sizes of the traces of multiple
estimated variables

## Usage

``` r
calc_summary_stats_traces(traces, sample_interval)
```

## Arguments

- traces:

  a data frame with traces of estimated parameters. Assumes the burn-ins
  are removed.

- sample_interval:

  the interval in timesteps between samples

## Value

the effective sample sizes

## See also

Use
[`remove_burn_ins`](https://docs.ropensci.org/tracerer/reference/remove_burn_ins.md)
to remove the burn-ins of all traces

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
estimates_all <- parse_beast_tracelog_file(
  get_tracerer_path("beast2_example_output.log")
)
estimates <- remove_burn_ins(estimates_all, burn_in_fraction = 0.1)

calc_summary_stats_traces(
  estimates,
  sample_interval = 1000
)
#>                           mean stderr_mean     stdev   variance      median
#> posterior          -70.5839432  0.50448873 1.6816291 2.82787643 -69.8797613
#> likelihood         -60.1725009  0.39642076 1.3214025 1.74610467 -60.0504225
#> prior              -10.4114423  0.54245052 1.8081684 3.26947291 -10.5950270
#> treeLikelihood     -60.1725009  0.39642076 1.3214025 1.74610467 -60.0504225
#> TreeHeight           0.9744748  0.14399367 0.3916244 0.15336965   0.8755907
#> BirthDeath          -3.5036870  0.54245052 1.8081684 3.26947291  -3.6872718
#> birthRate2           1.4470488  0.21344112 0.6713951 0.45077144   1.4118781
#> relativeDeathRate2   0.4937568  0.06502354 0.1709096 0.02921009   0.4480670
#>                    mode         geom_mean hpd_interval_low hpd_interval_high
#> posterior           n/a               n/a      -74.1526820       -68.6852294
#> likelihood          n/a               n/a      -62.4090389       -58.7371284
#> prior               n/a               n/a      -14.1703653        -7.2820933
#> treeLikelihood      n/a               n/a      -62.4090389       -58.7371284
#> TreeHeight          n/a  0.91041547166058        0.4529637         1.8159958
#> BirthDeath          n/a               n/a       -7.2626100        -0.3743380
#> birthRate2          n/a  1.28823302868404        0.3909076         2.8041208
#> relativeDeathRate2  n/a 0.466468860930895        0.2496224         0.7107459
#>                         act       ess
#> posterior          1000.000 10.000000
#> likelihood         1000.000 10.000000
#> prior              1000.000 10.000000
#> treeLikelihood     1000.000 10.000000
#> TreeHeight         1502.121  6.657254
#> BirthDeath         1000.000 10.000000
#> birthRate2         1122.942  8.905181
#> relativeDeathRate2 1608.296  6.217762
```
