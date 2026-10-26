# Removed the burn-in from a trace

Removed the burn-in from a trace

## Usage

``` r
remove_burn_in(trace, burn_in_fraction)
```

## Arguments

- trace:

  the values

- burn_in_fraction:

  the fraction that needs to be removed, must be \[0,1\>

## Value

the values with the burn-in removed

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
# Create a trace from one to and including ten
v <- seq(1, 10)

# Remove the first ten percent of its values,
# in this case removes the first value, which is one
w <- remove_burn_in(trace = v, burn_in_fraction = 0.1)
```
