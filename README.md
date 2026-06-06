# Δ-ML Reproduction

Reproduction of the Δ-machine learning approach for quantum chemistry,
using the MultiXC-QM9 dataset.

## Overview

This project implements the Δ-ML method introduced by Ramakrishnan et al. (2015),
which trains a machine learning model to predict the correction between a cheap
and an accurate quantum chemical method, rather than predicting the total energy directly:

E_predicted = E_cheap + ML(ΔE)

The reproduction uses the MultiXC-QM9 dataset, which provides molecular energies
for ~133k small organic molecules across 76 DFT functionals and 3 basis sets,
enabling systematic exploration of Δ-ML across many pairs of theory levels.

## References

**Method:**
Ramakrishnan, R.; Dral, P. O.; Rupp, M.; von Lilienfeld, O. A.
*Big Data Meets Quantum Chemistry Approximations: The Δ-Machine Learning Approach.*
J. Chem. Theory Comput. 2015, 11, 2087–2096.
DOI: [10.1021/acs.jctc.5b00099](https://doi.org/10.1021/acs.jctc.5b00099)

**Dataset:**
Nandi, S.; Vegge, T.; Bhowmik, A.
*MultiXC-QM9: Large dataset of molecular and reaction energies
from multi-level quantum chemical methods.*
Scientific Data 2023, 10, 783.
DOI: [10.1038/s41597-023-02690-2](https://doi.org/10.1038/s41597-023-02690-2)

## Project Structure

delta-ml-reproduction/
├── data/          # processed data files
├── notebooks/     # exploratory analysis
├── src/           # source code
├── results/       # figures and outputs
└── requirements.txt

## Environment

conda create -n delta-ml python=3.11
conda activate delta-ml
pip install -r requirements.txt
