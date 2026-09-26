# Parse all BEAST2 output files

Parse all BEAST2 output files

## Usage

``` r
parse_beast_output_files(log_filename, trees_filenames, state_filename)
```

## Arguments

- log_filename:

  deprecated name of the BEAST2 tracelog `.log` output file. Use
  `tracelog_filename` instead

- trees_filenames:

  the names of one or more a BEAST2 posterior `.trees` file. Each
  `.trees` file can be read using
  [parse_beast_trees](https://docs.ropensci.org/tracerer/reference/parse_beast_trees.md)

- state_filename:

  name of the BEAST2 state `.xml.state` output file

## Value

a list with the following elements:  

- `estimates`: parameter estimates

- `[alignment_id]_trees`: the phylogenies in the BEAST2 posterior.
  `[alignment_id]` is the ID of the alignment.

- `operators`: the BEAST2 MCMC operator acceptances

## See also

Use
[`remove_burn_ins`](https://docs.ropensci.org/tracerer/reference/remove_burn_ins.md)
to remove the burn-in from `out$estimates`

## Author

Richèl J.C. Bilderbeek

## Examples

``` r
trees_filenames <- get_tracerer_path("beast2_example_output.trees")
log_filename <- get_tracerer_path("beast2_example_output.log")
state_filename <- get_tracerer_path("beast2_example_output.xml.state")
parse_beast_output_files(
  log_filename = log_filename,
  trees_filenames = trees_filenames,
  state_filename = state_filename
)
#> $beast2_example_output_trees
#> 11 phylogenetic trees
#> 
#> $estimates
#>    Sample posterior likelihood      prior treeLikelihood TreeHeight BirthDeath
#> 1       0 -76.40152  -66.56126  -9.840263      -66.56126  0.6383792  -2.932508
#> 2    1000 -68.68523  -60.11853  -8.566701      -60.11853  0.7003758  -1.658946
#> 3    2000 -70.06839  -58.93807 -11.130319      -58.93807  1.4085182  -4.222564
#> 4    3000 -69.03990  -58.90834 -10.131561      -58.90834  0.9220334  -3.223806
#> 5    4000 -74.15268  -59.98232 -14.170365      -59.98232  1.8159958  -7.262610
#> 6    5000 -71.17163  -61.56657  -9.605062      -61.56657  0.7408032  -2.697307
#> 7    6000 -69.64176  -58.73713 -10.904631      -58.73713  1.0967406  -3.996876
#> 8    7000 -71.92546  -61.43600 -10.489461      -61.43600  1.0088078  -3.581706
#> 9    8000 -69.59441  -58.89381 -10.700593      -58.89381  0.8291479  -3.792838
#> 10   9000 -69.69113  -62.40904  -7.282093      -62.40904  0.4529637  -0.374338
#> 11  10000 -71.86884  -60.73520 -11.133636      -60.73520  0.7693617  -4.225880
#>    birthRate2 relativeDeathRate2
#> 1   1.0000000          0.5000000
#> 2   2.8041208          0.4952765
#> 3   0.7901276          0.3674313
#> 4   1.8637476          0.2496224
#> 5   1.7823070          0.3519155
#> 6   1.7849504          0.7085961
#> 7   1.1182466          0.3702605
#> 8   1.2610806          0.4008574
#> 9   0.3909076          0.5845426
#> 10  1.1123238          0.6983194
#> 11  1.5626756          0.7107459
#> 
#> $operators
#>            operator    p accept reject acceptFC rejectFC rejectIv rejectOp
#> 1      treeScaler.t 0.50    184    186        0        0        0        0
#> 2  treeRootScaler.t 0.50    144    224        0        0       63       63
#> 3 UniformOperator.t  NaN   2219   1667        0        0        0        0
#> 4    SubtreeSlide.t 1.00    409   1442        0        0      690      690
#> 5          narrow.t  NaN    962    972        0        0        0        0
#> 6            wide.t  NaN     50    349        0        0      236      236
#> 7   WilsonBalding.t  NaN     31    365        0        0      230      230
#> 8 BirthRateScaler.t 0.75    347     73        0        0        0        0
#> 9 DeathRateScaler.t 0.75    329     48        0        0        3        3
#> 
```
