# Calculate the auto-correlation time, alternative implementation

Calculate the auto-correlation time, alternative implementation

## Usage

``` r
calc_act(trace, sample_interval)
```

## Arguments

- trace:

  the values

- sample_interval:

  the interval in timesteps between samples

## Value

the auto_correlation time

## See also

Java code can be found here:
<https://github.com/CompEvol/beast2/blob/9f040ed0357c4b946ea276a481a4c654ad4fff36/src/beast/core/util/ESS.java#L161>
\# nolint URLs can be long

## Author

The original Java version of the algorithm was from Remco Bouckaert,
ported to R and adapted by Richèl J.C. Bilderbeek

## Examples

``` r
trace <- sin(seq(from = 0.0, to = 2.0 * pi, length.out = 100))
# 38.18202
calc_act(trace = trace, sample_interval = 1)
#> [1] 38.18202
```
