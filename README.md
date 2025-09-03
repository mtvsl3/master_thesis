# master_thesis
## Description
This project investigates the SPLEEN high-speed low-pressure (LPT) turbine through a numerical study in Nektar++. The problem was first implemented in Star-CCM+, which then was used to initialise the spectral/hp element method solver Nektar++

## Organisation
1. _parent_folder_ - contains all simulation files
2. msc_thesis - report
3. README - what you're currently reading

## Installation
Download the _parent_folder_ and unzip. This is assuming that the Nektar++ framework and Star-CCM+ are installed locally.

## Naming Convention
Three cases were run for different outlet Mach number values, with the following names:
- $M_{out}=0.7$  &rarr; _131_
- $M_{out}=0.9$  &rarr; _132_
- $M_{out}=0.95$  &rarr; _133_
All folders names are following the same convention: _CASE NUMBER + SETUP TYPE + P_, where
- CASE NUMBER - discussed above
- SETUP TYPE - _dim_ (for dimensional setup) or _nondim_ (for non-dimensional setup file)
- P - polynomial order
