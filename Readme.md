# Aerodyne-laser-chamber-fluxes
===============================

A python notebook to merge data from branch chambers, with gas concentrations measured using the Aerodyne Mini-TILDAS OCS/COS Monitor Laser (https://www.aerodyne.com/wp-content/uploads/2020/05/OCS_COS_Monitor.pdf). Data is gathered as follows:

(1) Gas concentrations: Aerodyne's built-in computer
(2) Reference concentration of CO2 and H2O: LI-COR LI-7000 infrared gas analyser (IRGA) which is part of a parallel system
(3) Photosynthetically active radiation, i.e. PAR: 1st Campbell CR1000 datalogger and
(4) Temperatures (air and leaf surface): 2nd Campbell CR1000 datalogger

There are 2 notebooks in this project, and the data is organised as follows:
(1) Raw data is in folder 01_rawdata, and logfiles are in 00_additional_data
(2) 01_convert_files_v0.1.ipynb: This creates daily files in a standard format in the folder 02_preprocessed_data
(3) 02_02_laser_v0.1.ipynb: This merges all data, removes bad data using the logbooks and calculates fluxes in the folder 03_processed_data

# Dependencies

The following python packages are required to read the FLIR files:

  - Pandas
  - Numpy
  - Scipy

# How to Cite

Jonathan D. Muller, Rafat Qubaja. (22 October 2020). Aerodyne-laser-chamber-fluxes: Tool to calculate gas fluxes from branch chambers. DOI: N/A (URL:
<N/A>), Python notebook

# License

This software is distributed under the GPL version 3

