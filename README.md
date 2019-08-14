# Fractional Differencing with GPU (GFD)

![](./assets/gfd_logo_transparent_resize.png)

<img src="https://img.shields.io/badge/license-MIT-green.svg"/>
<img src="https://img.shields.io/badge/version-v0.1-blue.svg"/>

This is a GPU implementation of fractional differencing (we call it GFD). It allows rapid large-scale implementation of fractional differencing to minimize memory loss while achieving stationary for time series data.

## Experiment Our Code Instantly Now on Google Colaboratory

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ritchieng/fractional_differencing_gpu/blob/master/notebooks/gpu_fractional_differencing.ipynb)

Easily run the whole tutorial in a self-contained Jupyter Notebook on Google Colaboratory by pressing the button above. The whole process of including pulling all data, dependencies and running the code for GFD is contained in the notebook, allowing you to run this notebook as is.

## Simple GFD Function

We've created a simple function in the notebook, pass your Pandas dataframe into the function and it will return fractionally differenced time series dataframe.
    - `d`: fractional differencing value, 0 means no differencing, above 1 means integer differencing, and anything between 0 to 1 is fractional differencing.
    - `floor`: minimum value to ignore for fixed window fractional differencing. 

**GPU implementation**

```python
gfd, weights = frac_diff_gpu(df_raw, d=0.5, floor=5e-5)
```

**CPU implementation**

```python
fd, weights = frac_diff(df_raw, d=0.5, floor=5e-5)
```

## Important Links to Presentation and Code Repository
- Code Repository: https://github.com/ritchieng/fractional_differencing_gpu
- Presentation: https://www.researchgate.net/publication/335159299_GFD_GPU_Fractional_Differencing_for_Rapid_Large-scale_Stationarizing_of_Time_Series_Data_while_Minimizing_Memory_Loss

## GFD Repository Plans
- Run GFD on thousands of time series datasets, creating a grid of t-stats and time benchmarks.
- Package GFD functions into a pip package for quick running

## Release Notes
This is an early beta release, we'll be releasing a stable release (v1.0) soon containing tests, more benchmarks, pip package and more. Please be patient!

## Citation Reference to Repository/Presentation
If you use the code, please cite using this [link](https://www.researchgate.net/publication/335159299_GFD_GPU_Fractional_Differencing_for_Rapid_Large-scale_Stationarizing_of_Time_Series_Data_while_Minimizing_Memory_Loss) alongside Prado/Hosking papers.

DOI: 10.13140/RG.2.2.19959.98727

## Credits and Special Thanks
1. NVIDIA (Ettikan, Chris and Nick), Amazon AWS, ensemblecap.ai, and NExT++ (NUS School of Computing)
2. Marcos Lopez de Prado  for his recent push on the use of fractional differencing of which this guide is based on.
3. Hosking for his paper in 1981 on fractional differencing.
