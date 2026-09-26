# Calculate the standard error of the mean

Calculate the standard error of the mean

## Usage

``` r
calc_stderr_mean(trace)
```

## Arguments

- trace:

  the values

## Value

the standard error of the mean

## See also

Java code can be found here:
<https://github.com/beast-dev/beast-mcmc/blob/800817772033c13061f026226e41128d21fd14f3/src/dr/inference/trace/TraceCorrelation.java#L159>
\# nolint URLs can be long

## Author

The original Java version of the algorithm was from Remco Bouckaert,
ported to R and adapted by Richèl J.C. Bilderbeek

## Examples

``` r
trace <- sin(seq(from = 0.0, to = 2.0 * pi, length.out = 100))
calc_stderr_mean(trace) # 0.4347425
#> [1] 0.4347425
```
