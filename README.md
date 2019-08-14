# Fractional Differencing with GPU (GFD)

<img src="https://img.shields.io/badge/license-MIT-green.svg"/>
<img src="https://img.shields.io/badge/version-v0.1-blue.svg"/>

This is a GPU implementation of fractional differencing (we call it GFD). It allows rapid large-scale implementation of fractional differencing to minimize memory loss while achieving stationary for time series data.

We've created a simple function in the notebook, pass your Pandas dataframe into the function and it will return fractionally differenced time series dataframe. 

## Experiment Our Code Instantly Now on Google Colaboratory

<a href="https://github.com/ritchieng/fractional_differencing_gpu/notebooks/gpu_fractional_differencing.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

Easily run the whole tutorial in a self-contained Jupyter Notebook on Google Colaboratory by pressing the button above. The whole process of including pulling all data, dependencies and running the code for GFD is contained in the notebook, allowing you to run this notebook as is.

## Important Links to Presentation and Code Repository
- Code Repository: https://github.com/ritchieng/fractional_differencing_gpu
- Presentation: 

## Summary of GFD

## GFD Repository Plans
- Run GFD on thousands of time series datasets, creating a grid of t-stats and time benchmarks.
- Package GFD functions into a pip package for quick running

## Release Notes
This is a early beta release, we'll be releasing a stable release (v1.0) soon containing tests, more benchmarks, pip package and more. Please be patient!

## Citation
If you use the code code, please use the following citation.
