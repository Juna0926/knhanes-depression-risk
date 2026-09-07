# Public Project Outputs

## Source artifact reviewed

- `국민건강영양조사·대기오염 연계 빅데이터 기반 우울증 위험군 예측 및 군집화 분석` — submitted analysis report for the Korean Society for Clinical Chemistry 2025 Fall Meeting healthcare big-data competition.

## Evidence included in this repository

- `assets/figure-01-cluster-feature-importance.svg` — representative factors reported for Cluster 0 and Cluster 1, without inventing unreported importance magnitudes.
- `assets/figure-02-subgroup-feature-importance.svg` — subgroup heterogeneity summarized from the report's cluster-level interpretation.
- `assets/figure-03-intervention-summary.svg` — policy/prevention considerations summarized from the report.

## Verified analysis structure

- KNHANES + linked air-pollution data
- 2014, 2016, 2020, 2022 waves
- 14,773 complete observations and 71 variables after preprocessing
- K-Means with K=5
- SMOTE for within-cluster class imbalance
- Model comparison followed by cluster-specific Random Forest interpretation

## Data note

The underlying KNHANES and linked environmental datasets are not redistributed. Users should obtain source data from the original providers and comply with their terms of use.
