# Public Project Outputs

## Source artifact reviewed

- `국민건강영양조사·대기오염 연계 빅데이터 기반 우울증 위험군 예측 및 군집화 분석` — submitted analysis report for the Korean Society for Clinical Chemistry 2025 Fall Meeting healthcare big-data competition.

## Current authoritative framing

The current README and Portfolio frame the project as:

**KNHANES health / lifestyle / socioeconomic / nutrition data + linked environmental exposure → K-Means subgroup profiling → within-cluster imbalance handling with SMOTE → subgroup-specific Random Forest depression-risk modeling**.

The analysis scale is **14,773 observations and 71 variables**, with **K=5** population subgroups and a final reported **average AUC of 0.7378**.

## Portfolio-aligned representative figure

- Portfolio source: `Juna0926/Portfolio/assets/media/project-knhanes-detail.svg`
- This figure reproduces the final report's cluster-profile summary and is now displayed as the primary README figure.

## Public file

- [`knhanes-analysis-public-excerpt.pdf`](knhanes-analysis-public-excerpt.pdf) — concise public-safe technical excerpt derived from the submitted report.

## Supporting repository evidence

- `assets/figure-01-cluster-feature-importance.svg` — representative factors reported for selected clusters, without inventing unreported importance magnitudes.
- `assets/figure-02-subgroup-feature-importance.svg` — subgroup heterogeneity summarized from the report's cluster-level interpretation.
- `assets/figure-03-intervention-summary.svg` — policy / prevention considerations summarized from the report.

## Verified analysis structure

- KNHANES + linked air-pollution data
- Survey waves: **2014, 2016, 2020, 2022**
- **14,773 observations**, **71 variables** after preprocessing
- **K-Means, K=5**
- **SMOTE** for within-cluster class imbalance
- candidate-model comparison followed by subgroup-specific **Random Forest** modeling and interpretation
- final portfolio-level performance summary: **average AUC 0.7378**

## Interpretation note

The five clusters are analytical population profiles, not clinical diagnoses. Feature importance and subgroup associations are descriptive / predictive results from observational pooled survey data and should not be interpreted causally.

## Data note

The underlying KNHANES and linked environmental datasets are not redistributed. Users should obtain source data from the original providers and comply with their terms of use.
