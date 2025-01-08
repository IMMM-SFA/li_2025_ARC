[![DOI](https://zenodo.org/badge/265254045.svg)](https://zenodo.org/doi/10.5281/zenodo.10442485)

<!-- Get rid of the metarepo instructions (the two sections below this) once you're done. -->

# metarepo
## [Check out the website for instructions](https://immm-sfa.github.io/metarepo)
`metarepo` is short for meta-repository, a GitHub repository that contains instructions to reproduce results in a published work. This repo is a template for creating your own metarepo.

## Purpose
A meta-repository creates a single point of access for someone to find all of the components that were used to create a published work for the purpose of reproducibility. This repository should contain references to all minted data and software as well as any ancillary code used to transform the source data, create figures for your publication, conduct the experiment, and / or execute the contributing software.

<!-- Get rid of the metarepo instructions (the two sections above this) once you're done. -->

# li_2025_ARC

**Bridging the gap between applied meteorology and climate science: a white roof example**

Dan Li<sup>1\*</sup>

<sup>1 </sup> Department of Earth and Environment and Department of Mechanical Engineering, Boston University, Boston, USA


\* corresponding author:  lidan@bu.edu

## Abstract
White roof is a widely-studied urban heat mitigation strategy and frequently incorporated into climate adaptation plans by cities.
Assessing the effects of white roofs on temperature has often been approached from the perspective of applied meteorology.
Here, the white roof problem is reframed to a climate science problem by focusing on the roof surface temperature, incorporating concepts of climate forcing, sensitivity, and feedback, and utilizing a linearized surface energy balance (SEB) model.
Different from the Albedo Cooling Effectiveness (ACE) index used for \textit{quantifying} white roof effects, a new index called Albedo Cooling Sensitivity ($\mathrm{ACS_s}$, where the subscript s indicates surface) is proposed as a stepping stone towards
\textit{understanding} white roof effects. The variability of $\mathrm{ACS_s}$ simulated by the Weather Research and Forecasting (WRF) model is found to be strongly related to the variability of convective heat transfer efficiency.
It is recommended that climate forcing, sensitivity, and feedback should be integrated into studying a wide range of urban adaptation strategies.


## Journal reference
Li et al. (in submission). Bridging the gap between applied meteorology and climate science: a white roof example

## Code reference

https://github.com/DanLi-BU/WRF/tree/WRF_ALBEDO (tag: ALB_final)

## Data reference

### Input data

Reference for each minted data source for your input data.  For example:

Human, I.M. (2021). My input dataset name [Data set]. DataHub. https://doi.org/some-doi-number

_your input data references here_

### Output data
Reference for each minted data source for your output data.  For example:

Human, I.M. (2021). My output dataset name [Data set]. DataHub. https://doi.org/some-doi-number

_your output data references here_


## Contributing modeling software
| Model | Version | Repository Link | Tag | DOI |
|-------|---------|-----------------|-----|-----|
| WRF | 4.2.2 | https://github.com/DanLi-BU/WRF/tree/WRF_ALBEDO | ALB_final | https://doi.org/10.5281/zenodo.14611848

## Reproduce my experiment
Fill in detailed info here or link to other documentation to thoroughly walkthrough how to use the contents of this repository to reproduce your experiment. Below is an example.

1. Install the software components required to conduct the experiment from [contributing modeling software](#contributing-modeling-software)
2. Download and install the supporting [input data](#input-data) required to conduct the experiment
3. Run the following scripts in the `workflow` directory to re-create this experiment:

| Script Name | Description | How to Run |
| --- | --- | --- |
| `namelist.input_July` | namelist to run the WRF part of the experiment of July |  |
| `namelist.input_Feb` | namelist to run the WRF part of the experiment of Feb |  |

4. change sf_sfclay_physics and bl_pbl_physics of all three domains to 2 for using MYJ
5. change sf_sfclay_physics and bl_pbl_physics of all three domains to 5 for using MYNN

## Reproduce my figures
Use the scripts found in the `figures` directory to reproduce the figures used in this publication. See details in the readme.docx document in

