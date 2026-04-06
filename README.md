# Prediction of Forest Fire Ignition Probabilities in Time with Survival Analysis

**Bachelor Thesis - DTU Compute, 2025**

**Author:** Hans Christian Zareh Lausten-Thomsen

## Abstract

This thesis frames wildfire ignition risk as a survival analysis problem and benchmarks three modelling approaches — Andersen-Gill Cox Proportional Hazards, Random Survival Forests, and DeepSurv — on spatio-temporal fire data from Campania (Italy) and the broader Mediterranean region. Models were evaluated under both spatial blocking and temporal splitting to assess generalisability and prevent data leakage.

Key contributions include time-varying feature engineering (fire history, neighbourhood risk, seasonal covariates), leakage-aware data preprocessing, and a thorough comparison of model discrimination (C-index), calibration (Brier scores), and feature importance across regions and validation schemes.

## Key Results

| Model | Campania (Spatial) | Campania (Temporal) | Mediterranean (Spatial) | Mediterranean (Temporal) |
|-------|-------------------|--------------------|-----------------------|------------------------|
| AG Cox | 0.800 | 0.838 | 0.811 | 0.869 |
| RSF | 0.814 | 0.865 | 0.863 | 0.905 |
| DeepSurv | 0.831 | 0.903 | — | — |

*Concordance index (C-index) across validation schemes.*

## Tools & Methods

- **Languages:** Python
- **Models:** Andersen-Gill Cox (lifelines), Random Survival Forests (scikit-survival), DeepSurv (PyTorch)
- **Evaluation:** C-index, Integrated Brier Score, calibration plots, permutation importance
- **Validation:** Spatial blocking (GroupKFold), temporal train/test splitting, bootstrap confidence intervals

## Thesis

The full thesis is available as [Fire_Ignition_modelling.pdf](Fire_Ignition_modelling-3.pdf) in this repository.
