[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/vlvovch/FIST-jupyter/master?filepath=FitExample.ipynb)


## Description

This repository contains an example using the [Thermal-FIST](https://github.com/vlvovch/Thermal-FIST) package in an interactive Jupyter session.
This is achieved through the [xeus-cling](https://github.com/QuantStack/xeus-cling) Jupyter kernel and a C++ interpreter [cling](https://github.com/root-project/cling)

The example presented here is designed for a Linux system. Other operating systems have not been tested. 

## Pre-requisites

A Python environment with [Jupyter Notebook](https://jupyter.org/) and [xeus-cling](https://github.com/QuantStack/xeus-cling) installed.

## Usage

1. Close this repository with the `--recurse-submodules` option to fetch the Thermal-FIST package automatically.
2. Build Thermal-FIST and Minuit2 as shared libraries:
    ```bash
    cd Thermal-FIST
    mkdir build
    cd build
    cmake -DBUILD_SHARED_LIBS=ON -DSTANDALONE_MINUIT=ON ../
    make ThermalFIST
    ```
    This will build the shared libraries in folder Thermal-FIST/build/lib.
 1. Run jupyter notebook from the repository root directory, open it in browser and try to execute the `FitExample.ipynb` notebook. If everything is in order, it will perform a thermal fit to ALICE 2.76 TeV Pb-Pb data.

## Attribution
Publications using **Thermal-FIST** should include a reference to the following paper:

- V. Vovchenko, H. Stoecker, *Thermal-FIST: A package for heavy-ion collisions and hadronic equation of state*, [arXiv:1901.05249 [nucl-th]](https://arxiv.org/abs/1901.05249)

*Copyright (C) 2019 Volodymyr Vovchenko*