[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5006796.svg)](https://doi.org/10.5281/zenodo.5006796)

# Aerodyne-laser-chamber-fluxes

A python notebook to merge data from branch chambers, with gas concentrations of H<sub>2</sub>O, CO<sub>2</sub>, COS and CO measured using the Aerodyne Mini-TILDAS OCS/COS Monitor Laser (https://www.aerodyne.com/wp-content/uploads/2020/05/OCS_COS_Monitor.pdf). Data is gathered as follows:

1. Gas concentrations: Aerodyne's built-in computer
2. Ambient concentration of CO<sub>2</sub> and H<sub>2</sub>O: LI-COR LI-7000 infrared gas analyser (IRGA) which is part of a parallel system
3. Photosynthetically active radiation, i.e. PAR: 1st Campbell CR1000 datalogger and
4. Temperatures (air and leaf surface): 2nd Campbell CR1000 datalogger

There are 2 notebooks in this project, and the data is organised as follows:
1. Raw data is in folder *01_rawdata*, and logfiles are in *00_additional_data*
2. **01_convert_files_v0.1.ipynb**: This creates daily files in a standard format in the folder *02_preprocessed_data*
3. **02_laser_v0.1.ipynb**: This merges all data, removes bad data using the logbooks and calculates fluxes in the folder *03_processed_data*. Data in this folder is organised as follows:
   * *raw_qc*: Data at the raw temporal resolution, merged with the unnecessary parts removed (i.e. stabilisation time of the laser)
   * *1min*: Of each measurement, the last 30-60 measurements in 1s intervals are taken. This folder contains averaged data of each measurement, with calculated fluxes.
   * *stats_calibration*: Statistics of the linear correlation done in daily steps. Each has the slope, intercept, R<sup>2</sup>, p-value, standard error and sample size (n).

## Dependencies

The following python packages are required to read the FLIR files:

  - Pandas
  - Numpy
  - Scipy

## How to Cite

Jonathan D. Muller, Rafat Qubaja. (2021). Aerodyne-laser-chamber-fluxes: Tool to calculate gas fluxes from branch chambers. DOI: 10.5281/zenodo.5006796  (URL:
<https://doi.org/10.5281/zenodo.5006796>), Python notebook

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5006796.svg)](https://doi.org/10.5281/zenodo.5006796)

## License

This software is distributed under the GNU GPL version 3

