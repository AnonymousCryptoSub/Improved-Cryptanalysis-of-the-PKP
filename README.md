# README

## Overview

This repository contains **experimental SageMath implementations** used
to validate the algorithms presented in our paper, titled "Improved Cryptanalysis of the Permuted Kernel Problem with Applications to PERK v2.2.0, SUSHSYFISH, and PKP-DSS".

------------------------------------------------------------------------

## Directory Structure

    .
    ├── Algorithm_1.sage      # Experimental verification of Algorithm 1 in the paper
    ├── Algorithm_2.sage      # Experimental verification of Algorithm 2 in the paper
    └── README.md             # This file

------------------------------------------------------------------------

## Requirements

### Dependencies

-    SageMath
-    NumPy
  


------------------------------------------------------------------------

## How to Run

Navigate to the directory containing the scripts and execute:

### Run Algorithm 1 / 2 experiment

``` bash
sage file_name
```



Each script:

1.  Generates a **random PKP instance** with a planted solution.
2.  Executes the corresponding algorithm.
3.  Prints:
    -   Collision counts
    -   Filtered candidate sizes
    -   Recovery success of the planted solution
    -   Aggregate statistics over trials

------------------------------------------------------------------------



## Purpose in the Paper

These scripts provide:

-   **Empirical validation** of Algorithm 1 and Algorithm 2


