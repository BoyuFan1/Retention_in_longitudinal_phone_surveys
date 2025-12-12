# Understanding retention in longitudinal surveys conducted by mobile phone in lower-resource contexts: A case study from Kenya

Code repository for the paper:

**Understanding retention in longitudinal surveys conducted by mobile phone in lower-resource contexts: A case study from Kenya**  
Corrina Moucheraud, Boyu Fan, Guanghao Li, Eric Ochieng, George Ganda, Ginger Golub, Alex Dahlen

This repo contains analysis code to:
- clean and harmonize baseline (2022) and follow-up (2024) survey datasets,
- construct retention outcomes (primary/secondary),
- run multiple imputation (MICE) for missing covariates,
- fit logistic regression models and pool estimates across imputations,

## Repository structure
- `notebooks/`
  - `Loss_to_Follow_Up.ipynb`
- `data/` *(not included; see below)*
  - `2022SurveyedPeople.dta`
  - `2024SurveyedPeople.dta`
- `outputs/` *(generated)*
  - `pooled_primary_logit.csv`, `pooled_primary_cov.csv`
  - `pooled_secondary_logit.csv`, `pooled_secondary_cov.csv`

## Data availability
The underlying survey data include human subjects information and are **not** publicly posted in this repository.  

## Requirements
Python packages used in the notebook:
- `pandas`, `numpy`, `scipy`, `statsmodels`
- `pyreadstat` (for `.dta` files)
- `miceforest` (for multiple imputation)

Example install:
```bash
pip install pandas numpy scipy statsmodels pyreadstat miceforest
