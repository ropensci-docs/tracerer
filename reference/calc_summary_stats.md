# Calculates the Effective Sample Sizes of one estimated variable's trace

Calculates the Effective Sample Sizes of one estimated variable's trace

## Usage

``` r
calc_summary_stats(traces, sample_interval)
```

## Arguments

- traces:

  one or more traces, supplies as either, (1) a numeric vector or, (2) a
  data frame of numeric values.

- sample_interval:

  the interval (the number of state transitions between samples) of the
  MCMC run that produced the trace. Using a different `sample_interval`
  than the actually used sampling interval will result in bogus return
  values.

## Value

the summary statistics of the traces. If one numeric vector is supplied,
a list is returned with the elements listed below. If the traces are
supplied as a data frame, a data frame is returned with the elements
listed below as column names.  
The elements are:  

- `mean`: mean

- `stderr_mean`: standard error of the mean

- `stdev`: standard deviation

- `variance`: variance

- `mode`: mode

- `geom_mean`: geometric mean

- `hpd_interval_low`: lower bound of 95% highest posterior density

- `hpd_interval_high`: upper bound of 95% highest posterior density

- `act`: auto correlation time

- `ess`: effective sample size

## Note

This function assumes the burn-in is removed. Use
[`remove_burn_in`](https://docs.ropensci.org/tracerer/reference/remove_burn_in.md)
(on a vector) or
[`remove_burn_ins`](https://docs.ropensci.org/tracerer/reference/remove_burn_ins.md)
(on a data frame) to remove the burn-in.

## See also

Use
[`calc_summary_stats_trace`](https://docs.ropensci.org/tracerer/reference/calc_summary_stats_trace.md)
to calculate the summary statistics of one trace (stored as a numeric
vector). Use
[`calc_summary_stats_traces`](https://docs.ropensci.org/tracerer/reference/calc_summary_stats_traces.md)
to calculate the summary statistics of more traces (stored as a data
frame).

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
estimates_all <- parse_beast_tracelog_file(
  get_tracerer_path("beast2_example_output.log")
)
estimates <- remove_burn_ins(estimates_all, burn_in_fraction = 0.1)

# From a single variable's trace
calc_summary_stats(
  estimates$posterior,
  sample_interval = 1000
)
#>        mean stderr_mean    stdev variance    median mode geom_mean
#> 1 -70.58394   0.5044887 1.681629 2.827876 -69.87976  n/a       n/a
#>   hpd_interval_low hpd_interval_high  act ess
#> 1        -74.15268         -68.68523 1000  10

# From all variables' traces
calc_summary_stats(
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
