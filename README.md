# Diabetes 30-Day Readmission Analysis

This course project examines 30-day hospital readmission among patients with diabetes using the publicly available [Diabetes 130-US Hospitals dataset](https://archive.ics.uci.edu/dataset/296/diabetes+130+us+hospitals+for+years+1999+2008). It demonstrates clinical data cleaning, exploratory analysis, and comparison of three classification models.

## Project workflow

1. `data_cleaning_final.ipynb` explores and cleans the source data, creates a binary 30-day readmission outcome, and exports `clean_diabetes.csv`.
2. `model_training.ipynb` uses the cleaned data to compare logistic regression, random forest, and XGBoost. It reports ROC-AUC, classification metrics, and visualizations.

## Results

On the held-out encounter-level test set, ROC-AUC was 0.569 for logistic regression, 0.609 for random forest, and 0.673 for XGBoost. These results come from a course analysis and should be interpreted as exploratory.

## Data and limitations

Download `diabetic_data.csv` from the UCI dataset page linked above and place it in the same folder as the notebooks before running them in order. The source data and generated CSV are not stored in this repository.

The dataset reflects historical hospital encounters from 1999–2008. The analysis splits encounters rather than patients, so encounters from the same person may appear in both training and test sets. Some preprocessing also occurs before the split. These limitations can make test performance optimistic. This project is not a clinically validated prediction tool.
