<p align="center">
  <img src="https://raw.githubusercontent.com/pygsflow/pygsflow/master/examples/figures/motto2.PNG" alt="pyGSFLOW logo"/>
</p>

[![pygsflow continuous integration](https://github.com/pygsflow/pygsflow/actions/workflows/ci.yml/badge.svg)](https://github.com/pygsflow/pygsflow/actions/workflows/ci.yml)
[![codecov](https://codecov.io/gh/pygsflow/pygsflow/branch/master/graph/badge.svg?token=UC4KRJAHUS)](https://codecov.io/gh/pygsflow/pygsflow)
[![PyPI](https://img.shields.io/pypi/v/pygsflow?style=plastic)](https://pypi.org/project/pygsflow/)
[![JOSS](https://joss.theoj.org/papers/d3989e65aedcc241930001cd32ba3a92/status.svg)](https://joss.theoj.org/papers/d3989e65aedcc241930001cd32ba3a92)

# pygsflow
pyGSFLOW is a python package to Create, Read, Write, Edit, and Visualize GSFLOW models

GSFLOW model development has previously been a piecemeal approach that required multiple software tools to build, edit, postprocess, and visualize models. pyGSFLOW changes this by being a tightly coupled scripting library that provides support for GSFLOW, PRMS, and MODFLOW. Custom modules for both GSFLOW and PRMS are included in this library. MODFLOW support is provided by wrapping the [Flopy](https://github.com/modflowpy/flopy) package (Bakker and others, 2021) with GSFLOW specific code. Together, these three pieces create a single integrated scripting package that helps to standardize and streamline model development and calibration. 

## API Documentation
pyGSFLOW API documentation can be found @

https://pygsflow.github.io/pygsflowdocs/

## Examples
Basic examples can be found in the Tutorial Examples tab of the pyGSFLOW API
documentation at https://pygsflow.github.io/pygsflowdocs/tutorials.html#

Interactive jupyter notebook example problems can be found in the examples directory.  
https://github.com/pygsflow/pygsflow/tree/master/examples

## Requirements
**Version 1.0.1** (Master branch and from pypi)
   1) Windows or Linux operating system (GSFLOW is not currently compiled for MacOS)  
   2) Python 3.6 or greater  
   3) FloPy 3.3.4 (`pip install flopy==3.3.4`)
   4) NetCdf4 (optional, required for netcdf exporting and autotesting) (`pip install netcdf4`)

**Version 1.1.0** (Develop branch)
   1) Windows or Linux operating system (GSFLOW is not currently compiled for MacOS)  
   2) Python 3.6 or greater 
   3) Flopy 3.3.4 or greater (`pip install flopy`) *note* for Python 3.6 use (`pip install flopy==3.3.4`)
   4) NetCdf4 (optional, required for netcdf exporting and autotesting) (`pip install netcdf4`)
   
## Installation
**Version 1.0.1** (Master branch and from pypi)
    
The pygsflow repository can be installed using pip.
To install the release version, open a terminal, command prompt, or anaconda prompt and type:

`pip install pygsflow`

or

`pip install https://github.com/pygsflow/pygsflow/zipball/master`

**Version 1.1.0** (Develop version with most recent updates)

To install the development version, open a terminal, command prompt or anaconda promt and type:  

`pip install https://github.com/pygsflow/pygsflow/zipball/develop`

Alternatively the user can download a copy of the repository, open a command prompt or anaconda promt terminal, cd into the trunk directory and type:

`pip install . `

**Additional Linux installation instructions**

To use the default version of GSFLOW for Linux that is distributed with pyGSFLOW the user
needs to set the permissions of the GSFLOW binary program to execute. From
a terminal window cd into the trunk/bin directory of the pyGSFLOW repository and
write:
```
chmod u+x gsflow
chmod u+x CRT_1.3.1
```

## Authors
Ayman Alzraiee, Joshua Larsen, Donald Martin, Rich Niswonger

## How to Cite

[Larsen, J. D., Alzraiee, A., Niswonger, R., 2021, pyGSFLOW v1.0.0: U.S. Geological
Survey Software Release, 2 July 2021, https://doi.org/10.5066/P9NPZ5AD](https://doi.org/10.5066/P9NPZ5AD)

## Bugs
The code is in active development and although there is a testing infrastructure set up we cannot catch all the software bugs without the help of users. If you find a bug or have an issue, please report it by opening a new issue. You can open a new issue by clicking the issues tab near the top of the page.

## Contributing
Please see [Contributing.md](https://github.com/pygsflow/pygsflow/blob/develop/CONTRIBUTING.md)

## Running Autotests Locally
pyGSFLOW uses github actions CI to automatically test code for each commit and pull request. These tests can also be run locally.
To run tests locally, navigate to pygsflow's root directory, open a command prompt, anaconda prompt, or terminal window:

with nosetests:
```
cd autotest
nosetests -v
```

with pytest:
```
cd autotest
pytest
```

*How to find pygsflow's root directory:*

Open a python terminal and type:
```python
import gsflow
print(gsflow.__file__)
```

## Project History
This project is a refinement and continuation of the original pygsflow repository at:

https://github.com/aymanalz/pygsflow

## Disclaimer
This software is preliminary or provisional and is subject to revision. It is being provided to meet the need for timely best science. The software has not received final approval by the U.S. Geological Survey (USGS). No warranty, expressed or implied, is made by the USGS or the U.S. Government as to the functionality of the software and related material nor shall the fact of release constitute any such warranty. The software is provided on the condition that neither the USGS nor the U.S. Government shall be held liable for any damages resulting from the authorized or unauthorized use of the software
