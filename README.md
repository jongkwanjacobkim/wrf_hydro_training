#  WRF-Hydro <img src="https://ral.ucar.edu/sites/default/files/public/wrf_hydro_symbol_logo_2017_09_150pxby63px.png" width=100 align="left" />

## Overview
This repository contains lessons in the form of Jupyter notebooks focused on understanding the basic functionality of WRF-Hydro.

### Requirements
The easiest and recommended way to run these lessons is via the [wrfhydro/hawaii-training](https://hub.docker.com/r/wrfhydro/hawaii-training/) Docker container, which has all software dependencies and data pre-installed.

* Docker >= v.17.12
* Web browser (Google Chrome recommended)

### Where to get help and/or post issues
If you have general questions about Docker, there are ample online resourves including the excellent Docker documentation at https://docs.docker.com/.

If you have questions about WRF-Hydro or these lessons please use the contact form on our website: https://ral.ucar.edu/projects/wrf_hydro/contact. 

If you happen to find a bug in these lessons please log an issue on the relevant GitHub repository: https://github.com/NCAR/wrf_hydro_training/issues.


## How to run
Confirm you have Docker installed and that it can access your localhost ports. Most out-of-the-box Docker installations accepting all defaults will have this configuration.

**Step 1: Open a terminal or PowerShell session**

**Step 2: Pull the wrfhydro/hawaii-training Docker container**
Issue the following command in your terminal.

`docker pull wrfhydro/hawaii-training`

**Step 3: Start the training container**
Issue the following commnand in your terminal to start the training Docker container.

`docker run --name wrf-hydro-training -p 8888:8888 -it wrfhydro/hawaii-training`
**Note: If you are restarting the training you will likely need to remove the previous container before reissuing the run command
`docker rm wrf-hydro-training`**

The container will start and perform a number of actions before starting the training. 

* First, the container will pull the model code.
* Second, the container will pull the relevant example test case.
* Third, the container will launch a Jupyter Lab server and echo the address to your terminal.

**Note: Port forwarding is setup with the `-p 8888:8888` argument, which maps your localhost port to the container port. If you already have sometihng running on port 8888 on your localhost you will need to change this number**
