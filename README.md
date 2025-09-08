# master_thesis
## Description
This project investigates the [SPLEEN high-speed low-pressure (LPT) turbine]([/guides/content/editing-an-existing-page#modifying-front-matter](https://www.h2020-spleen.eu/)) through a numerical study. The problem was first implemented in Star-CCM+, which then was used to initialise the spectral/hp element method solver Nektar++. Experimental data was obtained from: https://zenodo.org/records/13712768

## Organisation
1. _parent_folder_ - contains all simulation files
2. _master_thesis.pdf_ - master's thesis report
4. _guide_star.pdf_ - Star-CCM+ setup guide
5. _README_ - what you're currently reading

## Installation
Download the _parent_folder_ and unzip. This is assuming that the Nektar++ framework and Star-CCM+ are installed locally.

## Naming Convention
Three cases were run for different outlet Mach number values, with the following names:
- $M_{out}=0.7$  &rarr; _131_
- $M_{out}=0.9$  &rarr; _132_
- $M_{out}=0.95$  &rarr; _133_
  
All folders names are following the same convention: CASE NUMBER + SETUP TYPE + P, where
- CASE NUMBER - discussed above
- SETUP TYPE - _dim_ (for dimensional setup) or _nondim_ (for non-dimensional setup file)
- P - polynomial order

For example, folder named _133_nondim_p4_ corresponds to a case with $M_{out}=0.95$ with non-dimensional simulation setup and polynomial expansions of 4th order

## Scripts
1. _convert_and_copy_files_
## Star-CCM+
The problem was first implemented in Star-CCM+ with RANS resolution.

Folders:
1. _simulations_
  - .sim files for the three studied cases
2. _tables_
  - _convert_dimensions.py_ - Python code to convert the variables from primitive to conservative and to non-dimensionalise (if needed)
  - .csv files from Star-CCM+ with data that will be used to initialise Nektar++ (get automatically updated when Star-CCM+ simulations run until 800th iteration)
  - -csv files with converted data

Setup:
1. In Star-CCM+ navigate to _Tools > Tables_ and in each table, change the folder path to the relevent folder in your local repo to ensure the files are outputted in a correct place

## Nektar++ 

Setup:
1. Adjust the _parent_folder_ path in the _main.py_ script
