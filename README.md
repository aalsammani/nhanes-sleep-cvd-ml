# Interpretable Machine Learning Analysis of Sleep and Cardiovascular Disease Risk

This repository contains the reproducible analysis used for the project:

**Interpretable Machine Learning Analysis of Sleep and Cardiovascular Disease Risk Using NHANES Data (2013–2023)**

**Authors:** Imani Bush and Abdallah Alsammani  
**Institution:** Delaware State University  
**Program:** Delaware INBRE

## Overview

This project examines the association between sleep characteristics and cardiovascular disease (CVD) in U.S. adults and develops interpretable machine-learning models for CVD prediction.

The analysis compares:

- Balanced Logistic Regression
- Random Forest
- XGBoost

Model performance is evaluated using AUROC, AUPRC, recall, specificity, balanced accuracy, calibration, confusion matrices, and permutation feature importance.

## Main findings

- Long sleep (>9 hours) had the highest observed CVD prevalence.
- Balanced Logistic Regression achieved the highest AUPRC, recall, and balanced accuracy.
- Random Forest achieved the highest AUROC and specificity.
- Age was the strongest predictor, followed by hypertension, total cholesterol, race/ethnicity, and sleep-related variables.
- The adjusted sleep–CVD relationship suggested the lowest predicted risk near 7–8 hours of weekday sleep.

## Repository structure

```text
nhanes-sleep-cvd-ml/
│
├── README.md
├── NHANES_Sleep_CVD_Analysis.ipynb
│
├── figures/
│   ├── sleep_duration_distribution.png
│   ├── cvd_prevalence_by_sleep_category.png
│   ├── cvd_prevalence_by_sex_and_race.png
│   ├── clinical_measures_by_cvd_status.png
│   ├── spearman_correlation_matrix.png
│   ├── sleep_cvd_dose_response.png
│   ├── model_performance_metrics.png
│   ├── roc_and_precision_recall_curves.png
│   ├── calibration_and_confusion_matrix.png
│   └── permutation_feature_importance.png
│
└── docs/
    └── Project_Report.pdf
```

## Data

The raw and processed NHANES datasets are **not included** in this repository.

Place the analysis-ready CSV file in the same working directory expected by the notebook, or update the filename in the data-loading cell. See [`data/README.md`](data/README.md) for details.

NHANES data are publicly available from the U.S. Centers for Disease Control and Prevention.

## Installation

Create and activate a Python environment, then install the required packages:

```bash
python -m venv .venv
```

Windows:

```bash
.venv\Scripts\activate
```

macOS/Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Then open:

```text
notebooks/NHANES_Sleep_CVD_Analysis.ipynb
```

## Reproducibility

1. Place the required dataset in the expected location.
2. Open the notebook.
3. Select **Kernel → Restart & Run All**.
4. Confirm that all figures and tables are regenerated from the dataset.
5. Export figures at high resolution for manuscripts or posters.

## Important interpretation note

This is an observational, cross-sectional analysis. Reported associations do not establish causality. Survey design, self-reported variables, residual confounding, and missingness should be considered when interpreting results.

## License

Code is released under the MIT License. NHANES data remain subject to their original terms and are not redistributed here.

## Acknowledgment

This work was supported by the Delaware INBRE program, funded by the National Institute of General Medical Sciences of the National Institutes of Health.
