# SING

SING method implementation and code to reproduce results in corresponding paper

Risk, B. and Gaynanova, I. "Simultaneous Non-Gaussian Component Analysis (SING) for Data Integration in Neuroimaging"

## Main functions

**jngcaFunctions.R** - all the R functions needed for method's implementation and corresonding analyses

**CfunctionsCurvilinear.cpp** - additional C++ functions for implementation of curvilinear algorithm used for SING optimization; equivalent R functions can be found in **jngcaFunctions.R**

## Supporting data

**ComponentsForSim_setting2.Rda** - Shared and individual components used to simulate large-scale data for Simulation Setting 2

**community_affiliation_mmplus.csv** - File to support visualization of 

[here](https://www.nature.com/articles/s41598-019-55738-y).

## Simulations scripts

**s1_rank_simulations_small.R** - Simulation setting 1, rank estimation. (WARNING: this should only be run on a cluster as it takes significant time due to a total of 400 evaluations, and 1000 permutations for rank selection)

**s2_estimation_simulations_small.R** - Simulation setting 1, component and mixing matrices estimation performance. Can be run in parallel with s1.

**s3_results_analysis_small.R** - Simulation setting 1, uses the saved results from s1 and s2 to generate figures in the paper

**s4_generate_data_sim_setting2.R** - Simulation setting 2, uses the components in supplied .Rda file as true components to generate simulated data.

**s5_estimation_sim_setting2.R** - Simulation setting 2, apply joint ICA and SING with different value of rho, also apply rank estimation approach.

**s6_results_sim_setting2.R** - Simulation setting 2, use the results from s5 to calculate component and mixing matrix estimation errors, create figures in the paper.

