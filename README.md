<!--[![DOI](https://zenodo.org/badge/265254045.svg)](https://zenodo.org/doi/10.5281/zenodo.10442485)-->

<!-- Get rid of the metarepo instructions (the two sections below this) once you're done. -->
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

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.14624322.svg)](https://doi.org/10.5281/zenodo.14624322)

### Output data


## Contributing modeling software
| Model | Version | Repository Link | Tag | DOI |
|-------|---------|-----------------|-----|-----|
| WRF | 4.2.2 | https://github.com/DanLi-BU/WRF/tree/WRF_ALBEDO | ALB_final | https://doi.org/10.5281/zenodo.14611848

## Reproduce my experiment
Fill in detailed info here or link to other documentation to thoroughly walkthrough how to use the contents of this repository to reproduce your experiment. Below is an example.

1. Install the software components required to conduct the experiment from [contributing modeling software](#contributing-modeling-software)
2. Download and install the supporting [input data](#input-data) required to conduct the experiment.
wrfinput_d03 is for the control run, and wrfinput_d03_alb60 is for the high-albedo run.
Do NOT modify URBPARM.TBL when considering high albedo for roofs because modifying URBPARM.TBL will alter the roof albedo for all domains.
3. Use the following namelist.input in the [`scripts`](./scripts) directory to re-create this experiment:

| Script Name | Description | How to Run |
| --- | --- | --- |
| `namelist.input_July` | namelist to run the WRF experiment for July |  |
| `namelist.input_Feb` | namelist to run the WRF experiment for Feb |  |

4. change sf_sfclay_physics and bl_pbl_physics of all three domains to 2 for using MYJ
5. change sf_sfclay_physics and bl_pbl_physics of all three domains to 5 for using MYNN

## Reproduce my figures
Use the scripts found in the `figures` directory to reproduce the figures used in this publication.
