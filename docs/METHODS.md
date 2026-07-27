# Methods Summary

## Study design and data source

This observational analysis used publicly available National Health and Nutrition Examination Survey data covering 2013–2023. Survey modules were merged using the participant identifier `SEQN`.

## Outcome

A binary cardiovascular disease outcome was constructed from available self-reported cardiovascular-condition variables.

## Predictors

Predictors included demographic, sleep, lifestyle, and clinical variables. The displayed analysis includes age, sex, race/ethnicity, sleep duration, trouble sleeping, smoking, physical activity, hypertension, diabetes, body mass index, blood pressure, cholesterol, HbA1c, and income-to-poverty ratio where available.

## Preprocessing

- Missing continuous variables were imputed using the median.
- Missing categorical variables were imputed using the most frequent category.
- Continuous predictors were standardized when required.
- Categorical predictors were one-hot encoded.
- Data were divided using a stratified 80/20 train–test split.

## Models

- Balanced Logistic Regression
- Random Forest
- XGBoost

## Evaluation

Models were evaluated on the held-out test set using:

- AUROC
- AUPRC
- Recall
- Specificity
- Balanced accuracy
- Calibration curves
- Confusion matrices
- Permutation feature importance

AUPRC was emphasized because the CVD outcome was imbalanced.

## Statistical interpretation

Group comparisons and fitted associations should be interpreted as observational rather than causal. Confidence intervals and p-values do not eliminate the possibility of residual confounding or measurement error.
