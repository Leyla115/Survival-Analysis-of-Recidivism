# Survival Analysis of Recidivism
# Overview

This project explores the timing of recidivism (reoffending) among released prisoners using survival analysis methods in R. The analysis examines the impact of supervision and drug history on the probability and timing of committing a crime. Both non-parametric and parametric survival models are implemented, along with diagnostic tests and model comparisons.

# 1. Data Preparation

Loads a dataset from the Wooldridge collection.

Creates a binary variable indicating whether an individual committed a crime.

Prepares the data for survival analysis by checking structure and missing values.

# 2. Non-Parametric Survival Analysis

Estimates Kaplan-Meier survival curves for supervision and drug history groups.

Conducts log-rank tests to compare survival distributions.

Findings:

Supervision is associated with higher survival (lower recidivism).

Drug history is associated with lower survival (higher recidivism).

# 3. Hazard Rate Estimation

Estimates and plots hazard rates over time using kernel smoothing methods.

Observations:

Hazard rates decline over time for all groups.

Individuals with supervision have lower hazard rates.

Individuals with a drug history have higher hazard rates.

# 4. Cox Proportional Hazards Model

Fits Cox PH models including supervision, drug history, and other covariates.

Examines coefficients to assess the effect of supervision and drug history on recidivism risk.

Confirms that supervision reduces hazard rates while drug history increases hazard rates.

Tests proportional hazards assumption using various methods; results show no violations for key variables.

# 5. Parametric Survival Models

Estimates Exponential, Weibull, and Lognormal regression models including supervision and other covariates.

Calculates time ratios and hazard rate ratios for key variables:

Supervision increases average time to recidivism.

Drug history decreases average time to recidivism.

Prior criminal history increases hazard rates.

Compares models using Akaike Information Criterion (AIC).

Concludes that the lognormal model provides the best fit.

# Key Findings

Supervision reduces the probability of recidivism and extends the time until a potential reoffense.

Drug history increases the probability of recidivism and shortens the time to reoffense.

Hazard rates decline over time for all individuals.

Parametric survival models confirm the importance of supervision and drug history in predicting recidivism.

The lognormal model is preferred based on model fit criteria.

# Tools and Packages Used

dplyr, tidyr – Data manipulation and preparation

ggplot2 – Visualization of survival curves and hazard rates

survival – Kaplan-Meier, Cox PH models, and survival functions

muhaz – Kernel-based hazard rate estimation

stargazer – Tabular presentation of model results
