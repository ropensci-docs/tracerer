# Removed the burn-ins from a data frame

Removed the burn-ins from a data frame

## Usage

``` r
remove_burn_ins(traces, burn_in_fraction = 0.1)
```

## Arguments

- traces:

  a data frame with traces

- burn_in_fraction:

  the fraction that needs to be removed, must be `[0,1>`. Its default
  value of 10 as of Tracer

## Value

the data frame with the burn-in removed

## Author

Richèl J.C. Bilderbeek
