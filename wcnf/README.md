# MaxSAT Benchmark Instances

These databases contain information about MaxSAT benchmark instances taken from
[MaxSAT Lib](https://www.cs.toronto.edu/maxsat-lib/) and the [MaxSAT
Evaluations](https://maxsat-evaluations.github.io/).

Related to MaxSAT benchmark instances, we have the following databases.

| Database | Description |
| --- | --- |
| `wcnf_meta.db` | Metadata related to the benchmark instances |
| `wcnf_base.db` | Extracted base features of the benchmark instances |
| `wcnf_local.db` | Filenames and paths on the GBD server |
| `wcnf_tursolocal.db` | Filenames and paths on a University of Helsinki server |

## Metadata

`wcnf_meta.db` contains the following columns.

| Column | Description |
| --- | --- |
| `isohash` | Isomorphic hash to detect isomorphic instances |
| `weighted` | Whether the instance is weighted, i.e., does not only contain unit soft clauses |
| `partial` | Whether the instance is partial, i.e., contains hard clauses |
| `best_known_cost` | Cost of the best-known solution |
| `best_known_result` | Type of the best-known solution: `optimum`, `solution`, `mse list` if `best_known_cost` is taken from the list of MSE results without knowing where it came from |
| `family` | Instance family, typically a directory in MaxSAT Lib or the MSE sets |
| `track` | List of MSE tracks that the instance was used in; `<track>-<year>` |

## Base Features

`wcnf_base.db` contains the following columns.

| Column | Description |
| --- | --- |
| `base_features_runtime` | Runtime of the feature extractor |
| `h_clauses` | Number of hard clauses |
| `variables` | Number of variables |
| `h_cls<n>` | Number of hard clauses of length `<n>` (1-9) |
| `h_cls10p` | Number of hard clauses with at least 10 literals |
| `h_horn` | Number of hard horn clauses |
| `h_invhorn` | Number of hard inverse horn clauses |
| `h_positive` | |
| `h_negative` | |
| `h_hornvars_<dist>` | Distribution of horn variables on hard clauses |
| `h_invhornvars_<dist>` | Distribution of inverse horn variables on hard clauses |
| `h_balancecls_<dist>` | |
| `h_balancevars_<dist>` | |
| `s_clauses` | Number of soft clauses |
| `s_weight_sum` | Sum of all weights |
| `s_cls<n>` | Number of soft clauses of length `<n>` (1-9) |
| `s_cls10p` | Number of soft clauses with at least 10 literals |
| `s_weight_<dist>` | Distribution of weights |
| `h_vcg_vdegree_<dist>` | Distribution of variables degrees in variable clause graph |
| `h_vcg_cdegree_<dist>` | Distribution of clause degrees in variable clause graph |
| `h_vg_degree_<dist>` | Distribution of degrees in variable graph |
| `h_cg_degree_<dist>` | Distribution of degrees in clause graph |

Distributions features are `mean`, `variance`, `min`, `max` and `entropy`.
