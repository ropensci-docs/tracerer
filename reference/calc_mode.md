# Calculate the mode of values If the distribution is bi or multimodal or uniform, NA is returned

Calculate the mode of values If the distribution is bi or multimodal or
uniform, NA is returned

## Usage

``` r
calc_mode(values)
```

## Arguments

- values:

  numeric vector to calculate the mode of

## Value

the mode of the trace

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# In a unimodal distribution, find the value that occurs most
calc_mode(c(1, 2, 2))
#> [1] 2
calc_mode(c(1, 1, 2))
#> [1] 1

# For a uniform distribution, NA is returned
tracerer:::calc_mode(c(1, 2))
#> [1] NA
```
