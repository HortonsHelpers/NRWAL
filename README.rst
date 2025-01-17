*****************
Welcome to NRWAL!
*****************

.. image:: https://github.com/NREL/NRWAL/workflows/Documentation/badge.svg
    :target: https://nrel.github.io/NRWAL/

.. image:: https://github.com/NREL/NRWAL/workflows/Pytests/badge.svg
    :target: https://github.com/NREL/NRWAL/actions?query=workflow%3A%22Pytests%22

.. image:: https://github.com/NREL/NRWAL/workflows/Lint%20Code%20Base/badge.svg
    :target: https://github.com/NREL/NRWAL/actions?query=workflow%3A%22Lint+Code+Base%22

.. image:: https://img.shields.io/pypi/pyversions/NREL-NRWAL.svg
    :target: https://pypi.org/project/NREL-NRWAL/

.. image:: https://badge.fury.io/py/NREL-NRWAL.svg
    :target: https://badge.fury.io/py/NREL-NRWAL

.. image:: https://anaconda.org/nrel/nrel-NRWAL/badges/version.svg
    :target: https://anaconda.org/nrel/nrel-NRWAL

.. image:: https://anaconda.org/nrel/nrel-NRWAL/badges/license.svg
    :target: https://anaconda.org/nrel/nrel-NRWAL

.. image:: https://codecov.io/gh/nrel/NRWAL/branch/master/graph/badge.svg?token=3J5M44VAA9
    :target: https://codecov.io/gh/nrel/NRWAL

.. image:: https://zenodo.org/badge/319377095.svg
   :target: https://zenodo.org/badge/latestdoi/319377095

.. image:: https://mybinder.org/badge_logo.svg
    :target: https://mybinder.org/v2/gh/NREL/NRWAL/HEAD


.. inclusion-intro

The National Renewable Energy Laboratory Wind Analysis Library (NRWAL):

1. A library of wind cost equations
2. Dynamic python tools for intuitive equation handling
3. Ready-to-use configs for basic users
4. Easy equation manipulation without editing source code
5. One seriously badass sea unicorn

To get started with NRWAL, check out the `NRWAL Config documentation
<https://nrel.github.io/NRWAL/NRWAL/NRWAL.config.config.html>`_ or the
`NRWAL example notebook <https://github.com/NREL/NRWAL/blob/main/examples/example.ipynb>`_.
You can also launch the notebook in an interactive jupyter shell
right in your browser without any downloads or software using
`binder <https://mybinder.org/v2/gh/NREL/NRWAL/HEAD>`_.

Here is the important stuff:

`The NRWAL Equation Library <https://github.com/NREL/NRWAL/tree/main/NRWAL/analysis_library>`_.

`Default NRWAL Configs <https://github.com/NREL/NRWAL/tree/main/NRWAL/default_configs>`_.

`NRWAL Code Base <https://github.com/NREL/NRWAL/tree/master/NRWAL>`_.

Installing NRWAL
================

Option 1: Install from PIP or Conda (recommended for analysts):
---------------------------------------------------------------

1. Create a new environment:
    ``conda create --name nrwal``

2. Activate directory:
    ``conda activate nrwal``

3. Install reVX:
    1) ``pip install NREL-NRWAL`` or
    2) ``conda install nrel-nrwal --channel=nrel``

Option 2: Clone repo (recommended for developers)
-------------------------------------------------

1. from home dir, ``git clone https://github.com/NREL/NRWAL.git``
    1) enter github username
    2) enter github password

2. Create ``NRWAL`` environment and install package
    1) Create a conda env: ``conda create -n nrwal``
    2) Run the command: ``conda activate nrwal``
    3) cd into the repo cloned in 1.
    4) prior to running ``pip`` below, make sure the branch is correct (install
       from master!)
    5) Install ``NRWAL`` and its dependencies by running:
       ``pip install .`` (or ``pip install -e .`` if running a dev branch
       or working on the source code)

NRWAL Variables
===============

.. list-table:: NRWAL Inputs
    :widths: auto
    :header-rows: 1

    * - Variable Name
      - Long Name
      - Source
      - Units
    * - `aeff`
      - Array Efficiency
      - `array_efficiency` input layer, computed from ORBIT
      - `%`
    * - `capex_multi`
      - CAPEX Multiplier
      - Supplied by user
      - unit-less
    * - `depth`
      - Water depth (positive values)
      - `bathymetry` input layer
      - m
    * - `dist_a_to_s`
      - Distance from assembly area to site
      - Computed from `assembly_area` input layer
      - km
    * - `dist_op_to_s`
      - Distance from operating port to site
      - `ports_operations` input layer
      - km
    * - `dist_p_to_a`
      - Distance from port (construction no-limit) to assembly area
      - `assembly_area` input layer
      - km
    * - `dist_p_to_s`
      - Distance from construction port to site
      - `ports_construction` input layer
      - km
    * - `dist_p_to_s_nolimit`
      - Distance from no-limit construction port to site
      - `ports_construction_nolimit` input layer
      - km
    * - `dist_s_to_l`
      - Distance site to nearest land
      - `dist_to_coast` input layer
      - km
    * - `fixed_downtime`
      - Average weather downtime for fixed structure turbines
      - `weather_downtime_fixed_bottom` input layer
      - fraction
    * - `floating_downtime`
      - Average weather downtime for floating structure turbines
      - `weather_downtime_floating` input layer
      - fraction
    * - `gcf`
      - Gross capacity factor
      - Computed by reV / SAM with losses == 0
      - unit-less
    * - `hs_average`
      - Significant wave height to determine weather downtime
      - `weather_downtime_mean_wave_height_buoy` input layer
      - m
    * - `num_turbines`
      - Number of turbines in array
      - Supplied by user
      - unit-less
    * - `transmission_multi`
      - Tranmission cost multiplier
      - Supplied by user
      - unit-less
    * - `turbine_capacity`
      - Capacity of each turbine in the array
      - Supplied by user
      - MW

Recommended Citation
====================

Grant Buster, Jake Nunemaker, and Michael Rossol. The National Renewable Energy Laboratory Wind Analysis Libray (NRWAL). https://github.com/NREL/NRWAL (version v0.0.2), 2021. https://doi.org/10.5281/zenodo.4705961.
