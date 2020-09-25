## XROMS

`xroms` contains functions for commonly used scripts for working with ROMS output in xarray. 

There are functions to...
* help read in model output with automatically-calculated z coordinates
* calculate many derived variables with correct grid metrics in one line including:
  * horizontal speed
  * kinetic energy
  * eddy kinetic energy
  * vertical shear
  * vertical vorticity
  * Ertel potential vorticity
  * density as calculated in ROMS
  * potential density
  * buoyancy
  * N^2 (buoyancy frequency/vertical buoyancy gradient)
  * M^2 (horizontal buoyancy gradient)
* useful functions including:
  * derivatives in all dimensions, accounting for curvilinear grids and sigma layers
  * grid metrics (i.e., grid lengths, areas, and volumes)
  * easily change horizontal and vertical grids using `xgcm` grid objects
  * slice along a fixed value
  * mixed-layer depth
* Demonstrations:
  * selecting data in many different ways
  * interpolating in all dimensions, given `dask` chunks, sigma coordinates, and the fact that your grid might be curvilinear
  * changing time sampling
  * calculating climatologies
* provide meta data along with calculated variables


### Installation

You can install this locally and so that it is editable (`-e`), and with the required packages:

    git clone git@github.com:hetland/xroms.git
    cd xroms
    pip install -r requirements.txt -e .

Or:

    pip install git+git://github.com/hetland/xroms
    
Additionally installing [bottleneck](https://github.com/pydata/bottleneck/) is supposed to improve the speed of `numpy`-based calculations.