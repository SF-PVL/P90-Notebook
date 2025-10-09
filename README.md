# SunSolve P90 Uncertainty Analysis

This repository contains Python functions and tools for analyzing uncertainty in photovoltaic (PV) yield forecasts using [SunSolve](https://sunsolve.com)'s P90 client. The P90 client enables users to simulate uncertainty in their solar energy predictions, providing valuable insights for risk assessment and project planning.

## Overview

The P90 client helps solar energy analysts and engineers:
- Simulate uncertainty in PV yield forecasts
- Apply Gaussian, Weibull and Skewed Gaussian error functions to a variety of variables
- Apply errors on a global (simulation) level, yearly level and time-step level, independently
- Generate P90 (90th percentile) estimates for conservative planning, along with any other P-values
- Visualize yield histograms relative to the P50 yield of each year (does not estimate absolute yields)

## Repository Contents

- `P90 Analysis.ipynb` - Core Jupyter notebook containing the workflow to run uncertainty analysis on your system
- `UncertaintyFunctions.ipynb` - Helper Jupyter notebook containing Python functions for uncertainty analysis
- `pvl_p90_client-0.1.0.156+dev-py3-none-any.whl` - P90 client Python package
- `Data/` - Directory containing sample data files (e.g., `sydney.pvw`)
- `pvlib_P90_Comparison.ipynb` - Auxilliary Jupyter notebook containing a validation of the P90 client against pvlib
- `SunSolveLogo.svg` - SunSolve branding assets

## Usage

This repository is designed to be cloned directly within a Jupyter notebook environment (you may also simply [download it](https://github.com/SF-PVL/P90-Notebook/archive/refs/heads/main.zip) instead). The typical workflow is:

1. Clone this repository into your Jupyter environment `git clone https://github.com/SF-PVL/P90-Notebook.git`
2. Open `P90 Analysis.ipynb`
3. Run the initial cells, adjusting inputs as you go
4. When prompted, enter your pvlighthouse login details (VS Code will prompt you in the search bar)
5. Use the functions defined in the notebook to analyze your PV yield data in the remaining cells
6. Generate plots and visualizations of uncertainty results

## Getting Started

The `P90 Analysis.ipynb` notebook contains a full worked example for how to use the P90 client. Alternatively, you can follow the below steps:

```python
# Install the P90 client package
!pip install pvl_p90_client-0.1.0.156+dev-py3-none-any.whl

# Load the uncertainty functions notebook
%run UncertaintyFunctions.ipynb

# Your uncertainty analysis code here...
```

The functions in `UncertaintyFunctions.ipynb` provide tools for:
- Loading and preprocessing PV yield data
- Running uncertainty simulations
- Plotting results and uncertainty distributions
- Calculating P90 and other percentile estimates
- Comparing P90 results to pvlib result in `pvlib_P90_Comparison.ipynb`

## About SunSolve

[SunSolve](https://sunsolve.com) provides advanced solar energy simulation and analysis tools. The P90 client is part of SunSolve's suite of professional solar analytics solutions.