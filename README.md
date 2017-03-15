# CCA/EBT Experiments

This directory contains the raw results of the experiments reported in
an ICPE2017 paper: An Empirical Study of Computation-Intensive Loops for
Identifying and Classifying Loop Kernels.

We have selected approximately 1000 projects tagged with "language:FORTRAN"
hosted on [GitHub](https://github.com).
The loops from the projects were analyzed by [CCA/EBT](https://github.com/ebt-hpc/cca)
to obtain loop features.
From the loops, 100 are randomly sampled and are classified manually by a couple of
experienced performance engineers.

## Files

| File                | Description |
|---------------------|-------------|
|`metrics.csv`        | Source code metrics of 175,963 loops from 1020 projects hosted on GitHub |
|`judgments.csv`      | Manual classification results for the sampled 100 loops (comments written in Japanese) |
|`judgments-en.csv`   | Manual classification results for the sampled 100 loops (comments translated into English)|
|`training_set.csv`   | Training set for loop classification (M1--6, Other, NonKernel) |
|`training_set_k.csv` | Training set for loop classification (Kernel, NonKernel) |
|`training_set_m5.csv`| Training set for loop classification (M5, None: kernel other than M5) |

## Loop Features

| Feature | Description |
|-----------|-------------|
|`stmts`| Number of statements |
|`ops`| Number of operations |
|`fp_ops`| Number of floating-point operations |
|`branches`| Number of conditional statements |
|`calls`| Number of procedure/function calls |
|`array_refs0`| Number of array references (based on ES0) |
|`array_refs1`| Number of array references (based on ES1) |
|`array_refs2`| Number of array references (based on ES2) |
|`dbl_array_refs0`| Number of double array references (based on ES0) |
|`dbl_array_refs1`| Number of double array references (based on ES1) |
|`dbl_array_refs2`| Number of double array references (based on ES2) |
|`indirect_array_refs0`| Number of indirect array references (based on ES0) |
|`indirect_array_refs1`| Number of indirect array references (based on ES1) |
|`indirect_array_refs2`| Number of indirect array references (based on ES2) |
|`bf0`| B/F (based on ES0) |
|`bf1`| B/F (based on ES1) |
|`bf2`| B/F (based on ES2) |
|`lines_of_code`| Lines of code |
|`max_loop_depth`| Maximum loop depth |
|`max_loop_level`| Maximum loop nest level |
|`max_array_rank`| Maximum array rank |
|`max_mergeable_arrays`| Maximum number of meargeable arrays |
|`max_fusible_loops`| Maximum number of fusible arrays |
|`proj`| Project id |
|`ver`| Version |
|`path`| File path |
|`sub`| Surrounding subprogram name |
|`lnum`| Line number |
|`digest`| Hash value of the loop's AST|
|`nid`| Tree node id |
|`root_file`| File that contains the main program |

