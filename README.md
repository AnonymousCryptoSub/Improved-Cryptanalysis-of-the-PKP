# README

## Overview

This repository contains **experimental SageMath implementations** used
to validate the algorithms presented in our work on solving instances of
the **Permuted Kernel Problem (PKP)**.

Two scripts are provided:

-   **Algorithm_1.sage**\
    Experimental verification of **Algorithm 1**, implementing:
    -   Compatibility-table precomputation\
    -   Steinhaus--Johnson--Trotter (SJT) permutation updates\
    -   Random PKP instance generation with a planted solution\
    -   Algebraic reduction of the system\
    -   Meet-in-the-middle collision search\
    -   Measurement of raw and filtered collision statistics
-   **Algorithm_2.sage**\
    Experimental verification of **Algorithm 2**, which introduces a\
    **Schroeppel--Shamir--style time--memory trade-off**.\
    This script performs:
    -   Two-level SJT permutation precomputation\
    -   Random PKP instance generation with pairwise-distinct planted
        solution\
    -   Structured algebraic reduction\
    -   Two-stage meet-in-the-middle search\
    -   Collision counting, filtering, and recovery testing\
    -   Averaged empirical statistics over multiple trials

Both scripts use **small experimental parameters** to keep enumeration
feasible.

------------------------------------------------------------------------

## Directory Structure

    .
    ├── Algorithm_1.sage      # Experimental verification of Algorithm 1
    ├── Algorithm_2.sage      # Experimental verification of Algorithm 2
    └── README.md             # This file

------------------------------------------------------------------------

## Requirements

### Software

The code requires **SageMath** (recommended version ≥ 9.0).

Sage provides:

-   Finite-field arithmetic `GF(q)`
-   Linear algebra over finite fields
-   Random matrix/vector generation
-   Reduced row-echelon form (RREF)
-   Combinatorial utilities

### Installation

#### Linux / macOS

Install SageMath from:

https://www.sagemath.org/

Typical command-line usage after installation:

``` bash
sage --version
```

#### Using package managers (example)

``` bash
sudo apt install sagemath
```

------------------------------------------------------------------------

## How to Run

Navigate to the directory containing the scripts and execute:

### Run Algorithm 1 experiment

``` bash
sage Algorithm_1.sage
```

### Run Algorithm 2 experiment

``` bash
sage Algorithm_2.sage
```

Each script:

1.  Generates a **random PKP instance** with a planted solution.\
2.  Executes the corresponding algorithm.\
3.  Prints:
    -   Collision counts\
    -   Filtered candidate sizes\
    -   Recovery success of the planted solution\
    -   Aggregate statistics over trials

------------------------------------------------------------------------

## Experimental Parameters

Both scripts use **small fixed parameters** such as:

-   `n = 20` --- ambient dimension\
-   `m = 12` --- number of equations\
-   `q = 47` --- finite-field size

These values are chosen to:

-   Ensure **full enumeration is computationally feasible**\
-   Allow **statistical validation** of the algorithms\
-   Provide **sanity-check experimental confirmation** of theoretical
    analysis

They are **not intended for cryptographic-scale security evaluation**.

------------------------------------------------------------------------

## Reproducibility Notes

-   Randomness is drawn from Sage's internal RNG.\
-   To reproduce identical experiments, you may set a **fixed random
    seed** inside the scripts:

``` python
set_random_seed(0)
```

------------------------------------------------------------------------

## Purpose in the Paper

These scripts provide:

-   **Empirical validation** of Algorithm 1 and Algorithm 2\
-   **Collision-count measurements** supporting theoretical
    expectations\
-   **Recovery experiments** confirming correctness of the
    planted-solution framework\
-   **Evidence for the Schroeppel--Shamir time--memory trade-off in
    PKP**

They are intended **for research verification**, not optimized
implementations.

------------------------------------------------------------------------

## License / Usage

This code is released **for academic and research purposes**.\
Please cite the associated paper if you use or modify the
implementation.
