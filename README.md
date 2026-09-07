# Depression Risk Profiling with KNHANES & Air-Pollution Data

> Population-health analysis that combines national health-survey data with environmental exposure, then models depression risk within heterogeneous subgroups rather than treating the population as one homogeneous cohort.

**Period:** 2025  
**Affiliation:** Machine Learning & Data Mining Laboratory, Ajou University  
**Output:** Korean Society for Clinical Chemistry 2025 Fall Meeting - Healthcare Big Data Analysis Competition report  
**Role:** Representative / project lead listed on the submitted report  
**Core methods:** K-Means · SMOTE · Random Forest

---

## Overview

The project combines **KNHANES** health-survey records with linked air-pollution variables to investigate multidimensional factors associated with depressive symptoms. The analysis was designed around population heterogeneity: participants were first grouped by risk-profile characteristics, and predictive factors were then interpreted within each subgroup.

## Data pipeline

The submitted analysis used data from **2014, 2016, 2020, and 2022** and merged examination, health-questionnaire, nutrition, and environmental-exposure variables.

After staged validity / missing-data processing and feature reduction, the complete analysis dataset contained:

- **14,773 observations**
- **71 variables**
- one-hot encoding for categorical variables
- scaling for continuous variables

Raw KNHANES / linked environmental data are not redistributed in this repository.

## Modeling strategy

1. Integrate health, behavioral, socioeconomic, nutritional, and air-pollution variables.
2. Use **K-Means (K=5)** to derive distinct participant profiles.
3. Address within-cluster class imbalance using **SMOTE**.
4. Compare classification models.
5. Use cluster-specific **Random Forest** models for interpretable feature importance.
6. Translate subgroup-specific risk patterns into differentiated intervention considerations.

## Results & interpretation

The submitted report found that the most important variables differed substantially by cluster. Examples included nutritional / chronic-disease factors in older low-energy groups, lifestyle and social-support factors in younger groups, and environmental exposure in a middle-aged fine-dust-exposed profile.

![Cluster-specific feature importance](assets/figure-01-cluster-feature-importance.png)

![Additional subgroup feature importance](assets/figure-02-subgroup-feature-importance.png)

The value of the approach is therefore not a single universal feature ranking, but the identification of **different risk structures across population subgroups**.

![Intervention summary](assets/figure-03-intervention-summary.png)

## My contribution

The submitted report lists **Junha Won as representative author**, with Seungju Jung and Seunghyun Park as team members. The project covered:

- Data integration and preprocessing
- Clustering and imbalance handling
- Machine-learning model comparison
- Cluster-specific feature-importance analysis
- Interpretation of risk profiles and intervention implications
- Competition report preparation

## Project output

- [`outputs/knhanes-air-pollution-depression-analysis-report.pdf`](outputs/knhanes-air-pollution-depression-analysis-report.pdf) - full submitted analysis report.

## Limitations

This is an observational, cross-sectional / pooled survey analysis and should not be interpreted as establishing causal effects of individual risk factors. Cluster labels are analytical profiles rather than clinical diagnoses.

---

**Junha Won** · Ajou University  
[Portfolio](https://juna0926.github.io/Portfolio/) · [GitHub](https://github.com/Juna0926)
