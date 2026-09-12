# Package index

## All functions

- [`calc_act()`](https://docs.ropensci.org/tracerer/reference/calc_act.md)
  : Calculate the auto-correlation time, alternative implementation

- [`calc_act_cpp()`](https://docs.ropensci.org/tracerer/reference/calc_act_cpp.md)
  :

  Calculate the auto correlation time from
  <https://github.com/beast-dev/beast-mcmc/blob/800817772033c13061f026226e41128d21fd14f3/src/dr/inference/trace/TraceCorrelation.java#L159>
  \# nolint

- [`calc_act_r()`](https://docs.ropensci.org/tracerer/reference/calc_act_r.md)
  : Calculate the auto-correlation time using only R. Consider using
  calc_act instead, as it is orders of magnitude faster

- [`calc_ess()`](https://docs.ropensci.org/tracerer/reference/calc_ess.md)
  : Calculates the Effective Sample Size

- [`calc_esses()`](https://docs.ropensci.org/tracerer/reference/calc_esses.md)
  : Calculates the Effective Sample Sizes from a parsed BEAST2 log file

- [`calc_geom_mean()`](https://docs.ropensci.org/tracerer/reference/calc_geom_mean.md)
  : Calculate the geometric mean

- [`calc_hpd_interval()`](https://docs.ropensci.org/tracerer/reference/calc_hpd_interval.md)
  : Calculate the Highest Probability Density of an MCMC trace that has
  its burn-in removed

- [`calc_mode()`](https://docs.ropensci.org/tracerer/reference/calc_mode.md)
  : Calculate the mode of values If the distribution is bi or multimodal
  or uniform, NA is returned

- [`calc_std_error_of_mean_cpp()`](https://docs.ropensci.org/tracerer/reference/calc_std_error_of_mean_cpp.md)
  : Calculates the standard error of the mean

- [`calc_stderr_mean()`](https://docs.ropensci.org/tracerer/reference/calc_stderr_mean.md)
  : Calculate the standard error of the mean

- [`calc_summary_stats()`](https://docs.ropensci.org/tracerer/reference/calc_summary_stats.md)
  : Calculates the Effective Sample Sizes of one estimated variable's
  trace

- [`calc_summary_stats_trace()`](https://docs.ropensci.org/tracerer/reference/calc_summary_stats_trace.md)
  : Calculates the Effective Sample Sizes of one estimated variable's
  trace

- [`calc_summary_stats_traces()`](https://docs.ropensci.org/tracerer/reference/calc_summary_stats_traces.md)
  : Calculates the Effective Sample Sizes of the traces of multiple
  estimated variables

- [`check_trace()`](https://docs.ropensci.org/tracerer/reference/check_trace.md)
  :

  Check if the trace is a valid. Will
  [stop](https://rdrr.io/r/base/stop.html) if not

- [`count_trees_in_file()`](https://docs.ropensci.org/tracerer/reference/count_trees_in_file.md)
  :

  Count the number of trees in a `.trees` file

- [`cs_std_dev()`](https://docs.ropensci.org/tracerer/reference/cs_std_dev.md)
  : Calculate the corrected sample standard deviation

- [`default_params_doc()`](https://docs.ropensci.org/tracerer/reference/default_params_doc.md)
  : Documentation of general function arguments

- [`extract_operators_lines()`](https://docs.ropensci.org/tracerer/reference/extract_operators_lines.md)
  :

  Extract the JSON lines out of a `.xml.state` with the unparsed BEAST2
  MCMC operator acceptances file with the operators

- [`get_tracerer_path()`](https://docs.ropensci.org/tracerer/reference/get_tracerer_path.md)
  :

  Get the full path of a file in the `inst/extdata` folder

- [`get_tracerer_paths()`](https://docs.ropensci.org/tracerer/reference/get_tracerer_paths.md)
  :

  Get the full paths of files in the `inst/extdata` folder

- [`get_tracerer_tempfilename()`](https://docs.ropensci.org/tracerer/reference/get_tracerer_tempfilename.md)
  : Get a temporary filename

- [`is_posterior()`](https://docs.ropensci.org/tracerer/reference/is_posterior.md)
  : Determines if the input is a BEAST2 posterior

- [`is_trees_file()`](https://docs.ropensci.org/tracerer/reference/is_trees_file.md)
  :

  Measure if a file a valid BEAST2 `.trees` file

- [`is_trees_posterior()`](https://docs.ropensci.org/tracerer/reference/is_trees_posterior.md)
  : Determines if the input is a BEAST2 posterior, as parsed by
  parse_beast_trees

- [`parse_beast_log()`](https://docs.ropensci.org/tracerer/reference/parse_beast_log.md)
  :

  Deprecated function to parse a BEAST2 `.log` output file. Use
  parse_beast_tracelog_file instead

- [`parse_beast_output_files()`](https://docs.ropensci.org/tracerer/reference/parse_beast_output_files.md)
  : Parse all BEAST2 output files

- [`parse_beast_posterior()`](https://docs.ropensci.org/tracerer/reference/parse_beast_posterior.md)
  : Parses BEAST2 output files to a posterior

- [`parse_beast_state_operators()`](https://docs.ropensci.org/tracerer/reference/parse_beast_state_operators.md)
  :

  Parses a BEAST2 state `.xml.state` output file to get only the
  operators acceptances

- [`parse_beast_tracelog_file()`](https://docs.ropensci.org/tracerer/reference/parse_beast_tracelog_file.md)
  :

  Parses a BEAST2 tracelog `.log` output file

- [`parse_beast_trees()`](https://docs.ropensci.org/tracerer/reference/parse_beast_trees.md)
  : Parses a BEAST2 .trees output file

- [`remove_burn_in()`](https://docs.ropensci.org/tracerer/reference/remove_burn_in.md)
  : Removed the burn-in from a trace

- [`remove_burn_ins()`](https://docs.ropensci.org/tracerer/reference/remove_burn_ins.md)
  : Removed the burn-ins from a data frame

- [`save_beast_estimates()`](https://docs.ropensci.org/tracerer/reference/save_beast_estimates.md)
  :

  Save the BEAST2 estimates as a BEAST2 `.log` file There will be some
  differences: a BEAST2 `.log` file also saves the model as comments and
  formats the numbers in a way non-standard to R

- [`save_beast_trees()`](https://docs.ropensci.org/tracerer/reference/save_beast_trees.md)
  :

  Save the BEAST2 trees as a BEAST2 `.log` file There will be some
  differences: a BEAST2 `.log` file also saves the model as comments and
  formats the numbers in a way non-standard to R
