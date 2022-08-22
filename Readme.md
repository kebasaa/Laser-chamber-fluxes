[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4117838.svg)](https://doi.org/10.5281/zenodo.4117838)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

# Laser-chamber-fluxes

A python notebook to merge data from chamber systems, with gas concentrations of H<sub>2</sub>O, CO<sub>2</sub>, COS and CO measured using the Aerodyne Mini-TILDAS OCS/COS Monitor QCL Laser (https://www.aerodyne.com/wp-content/uploads/2021/11/OCS_COS.pdf). Data is gathered as follows:

1. Gas concentrations: Aerodyne's built-in computer
2. Ambient concentration of CO<sub>2</sub> and H<sub>2</sub>O: LI-COR LI-7000 infrared gas analyser (IRGA) which is part of a parallel system
3. Photosynthetically active radiation, i.e. PAR: 1st Campbell CR1000 datalogger and
4. Temperatures (air and leaf surface): 2nd Campbell CR1000 datalogger
5. Thermocouples (e.g. air or surface): 3rd Campbell CR1000 datalogger

There are 2 notebooks in this project, and the data is organised as follows:
1. Raw data is in folder *01_rawdata*, and logfiles are in *00_additional_data*
2. **01_convert_files_v0.1.ipynb**: This creates daily files in a standard format in the folder *02_preprocessed_data*
3. **02_laser_v0.1.ipynb**: This merges all data, removes bad data using the logbooks and calculates fluxes in the folder *03_processed_data*. Data in this folder is organised as follows:
   * *raw_qc*: Data at the raw temporal resolution, merged with the unnecessary parts removed (i.e. stabilisation time of the laser)
   * *1min*: Of each measurement, the last 30-60 measurements in 1s intervals are taken. This folder contains averaged data of each measurement, with calculated fluxes.
   * *stats_calibration*: Statistics of the linear correlation done in daily steps. Each has the slope, intercept, R<sup>2</sup>, p-value, standard error and sample size (n).

## Dependencies

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)

The following python packages are required to read the FLIR files:

  - Pandas
  - Numpy
  - Scipy

## How to Cite

Jonathan D. Muller. (2022). Laser-chamber-fluxes: Tool to calculate gas fluxes from chambers concentration measurements. DOI: 10.5281/zenodo.4117838  (URL:
<https://doi.org/10.5281/zenodo.4117838>), Python notebook

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4117838.svg)](https://doi.org/10.5281/zenodo.4117838)

## License

This software is distributed under the GNU GPL version 3

