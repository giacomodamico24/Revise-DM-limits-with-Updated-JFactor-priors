# Revising DM Limits with Updated J-Factor Priors

This repository provides a general and practical framework to update published upper limits on the dark matter annihilation cross section when improved determinations of astrophysical J-factor priors become available.

The method consistently propagates revised J-factor information into existing likelihood-based limits, enabling results to evolve alongside improved halo modeling without requiring a full reanalysis of the original data.

## Repository Structure

The repository includes two Jupyter notebooks that reproduce key validation results presented in the paper:

### Test_with_Toy_MCs.ipynb  

This notebook reproduces Figure 1 of the paper.
It validates the updating procedure in a controlled toy Monte Carlo setup for a single target, considering:
- Gaussian J-factor prior
- Log-normal J-factor prior


### Combine_ULs.ipynb

This notebook reproduces Figure 3 of the paper.
It validates the method in the multi-target case, where the combined likelihood is constructed as the sum of individual target contributions.


## Requirements

The notebooks were developed and tested with the following package versions:
-	Python ≥ 3.10
- numpy == 1.26.4
- scipy == 1.11.4
- astropy == 5.1.1
- matplotlib == 3.8.4

The code relies on:
- scipy.optimize (minimize, brentq)
- scipy.special.lambertw
- astropy.table and astropy.units


## Purpose

This repository is intended to:
- Provide a transparent implementation of the updating framework
- Allow full reproducibility of results from the paper
- Serve as a reference for applying the method to other datasets
