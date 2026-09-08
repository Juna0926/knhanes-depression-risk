# Depression Risk Prediction Using KNHANES Data

> Subgroup-specific depression-risk profiling using KNHANES health-survey data and linked air-pollution variables.

**Period:** Jun. 2025 - Sep. 2025  
**Affiliation:** Machine Learning & Data Mining Laboratory, Ajou University  
**Core methods:** K-Means · SMOTE · Random Forest  
**Final reported performance:** Average AUC **0.7378**

---

## Overview

This project combined **KNHANES** health-survey records with linked air-pollution data to analyze depression risk across a heterogeneous population. Rather than assuming that one universal risk structure applies to everyone, the analysis first identified participant subgroups and then examined depression-risk patterns within each subgroup.

The final workflow integrated health, lifestyle, socioeconomic, nutritional, chronic-disease, and environmental-exposure variables into a subgroup-specific machine-learning pipeline.

## Data pipeline

The submitted analysis used data from **2014, 2016, 2020, and 2022** and combined examination, health-questionnaire, nutrition, and environmental-exposure variables.

After staged validity / missing-data processing and feature reduction, the analysis dataset contained:

- **14,773 observations**
- **71 variables**
- one-hot encoding for categorical variables
- scaling for continuous variables

Raw KNHANES and linked environmental data are not redistributed in this repository.

## Modeling strategy

1. Integrate health, behavioral, socioeconomic, nutritional, chronic-disease, and air-pollution variables.
2. Use **K-Means (K=5)** to derive participant profiles.
3. Address within-cluster class imbalance using **SMOTE**.
4. Compare candidate classifiers.
5. Use subgroup-specific **Random Forest** models for prediction and feature-importance interpretation.
6. Compare risk structures across clusters and translate them into differentiated intervention considerations.

## Main result

The final portfolio version reports an **average AUC of 0.7378** across the subgroup-specific depression-risk modeling pipeline.

The most important predictors differed substantially by cluster, showing that depression-risk structure was not uniform across the population. Examples included chronic-disease and nutritional factors in older low-energy groups, lifestyle and social-support factors in younger groups, and environmental exposure in a middle-aged fine-dust-exposed profile.

![Cluster-specific feature importance](assets/figure-01-cluster-feature-importance.svg)

![Subgroup heterogeneity](assets/figure-02-subgroup-feature-importance.svg)

The main value of the project is therefore not a single global feature ranking, but the identification of **different depression-risk structures across population subgroups**.

![Intervention summary](assets/figure-03-intervention-summary.svg)

## Project provenance

The submitted report lists **Junha Won as representative author**, with Seungju Jung and Seunghyun Park as co-authors. This repository documents the report's data integration, subgroup modeling, feature-importance interpretation, and intervention framing without claiming individual contribution beyond what the source materials support.

## Public outputs

- [`outputs/knhanes-analysis-public-excerpt.pdf`](outputs/knhanes-analysis-public-excerpt.pdf) - concise public-safe technical excerpt derived from the submitted competition report.
- [`outputs/PROJECT_OUTPUTS.md`](outputs/PROJECT_OUTPUTS.md) - source provenance, verified analysis structure, and public-release notes.

## Limitations

This is an observational, cross-sectional / pooled survey analysis and should not be interpreted as establishing causal effects of individual risk factors. Cluster labels represent analytical profiles rather than clinical diagnoses.

---

**Junha Won** · Ajou University  
[Portfolio detail](https://juna0926.github.io/Portfolio/projects/knhanes.html) · [Portfolio](https://juna0926.github.io/Portfolio/) · [GitHub](https://github.com/Juna0926)
