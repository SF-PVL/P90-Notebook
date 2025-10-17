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
- `pvl_p90_client-0.1.0.167+prerelease-py3-none-any.whl` - P90 client Python package
- `Data/` - Directory containing sample data files (e.g., `sydney.pvw`)
- `pvlib_P90_Comparison.ipynb` - Auxilliary Jupyter notebook containing a validation of the P90 client against pvlib
- `SunSolveLogo.svg` - SunSolve branding assets

## Requirements
* Google Colab; **OR** the below:
* Python 3+ (https://www.python.org/downloads/)
* pip 20+ (https://pypi.org/project/pip/ )
* Jupyter (run `pip install jupyter` from terminal)
* numpy, scipy, matplotlib, plotly, pandas (run `pip install numpy scipy matplotlib plotly pandas` from terminal)
* git (for cloning the repository, alternatively you may just [download it](https://github.com/SF-PVL/P90-Notebook/archive/refs/heads/main.zip) manually)

## Getting Started

### Using Google Colab

Follow steps in [colab.research.google.com/github/SF-PVL/P90-Notebook](https://colab.research.google.com/github/SF-PVL/P90-Notebook/blob/main/P90%20Analysis.ipynb) and avoid `USING_DRIVE` for the simplest experience.

To save files, you will need to use connect to Google Drive and change the folder variable to the Drive folder of your choice. Also change `USING_DRIVE` to `True`.

You can always just save files manually without Drive, but they will be lost forever if the session times out from inactivity (90 minutes).

### Using Jupyter and Python locally

Assuming you have installed all requirements:

[Download](https://github.com/SF-PVL/P90-Notebook/archive/refs/heads/main.zip) (or clone) the SunSolve P90 GitHub repository into your preferred folder.
(`git clone https://github.com/SF-PVL/P90-Notebook.git`)

From this folder run  jupyter notebook from a terminal to start the notebook app in-browser.
(**VS Code users**: skip this step)

From the notebook app, open the P90 Analysis.ipynb notebook.
(**VS Code users**: simply open the notebook and choose a kernel when prompted. ‘venv’ is default)

Run the initial cells, adjusting inputs as you go.

When prompted, enter your PV Lighthouse login details in the prompt below **Code cell 1**.
(**VS Code users**: prompt appears in the search bar at the top of the window)

Use the functions defined in the notebook to analyse your PV yield data in the remaining cells.

Generate plots and visualizations of uncertainty results.

## About SunSolve

[SunSolve](https://sunsolve.com) provides advanced solar energy simulation and analysis tools. The P90 client is part of SunSolve's suite of professional solar analytics solutions.