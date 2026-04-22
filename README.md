# EDA Chronic Kidney Disease CKD Data

This project is an Exploratory Data Analysis (EDA) of a Chronic Kidney Disease (CKD) dataset.

## Dataset

The analysis uses the `kidney_disease.csv` file included in this repository.

Based on the file name, row and column pattern, and medical features, this dataset appears to match the original UCI Chronic Kidney Disease dataset:
[UCI Chronic Kidney Disease Dataset](https://archive.ics.uci.edu/ml/datasets/chronic_kidney_disease)

The dataset includes medical and health-related features such as:
- age
- blood pressure
- specific gravity
- albumin
- sugar
- red blood cells
- pus cells
- blood glucose random
- blood urea
- serum creatinine
- sodium
- potassium
- haemoglobin
- packed cell volume
- white blood cell count
- red blood cell count
- hypertension
- diabetes mellitus
- coronary artery disease
- appetite
- pedal edema
- anemia
- CKD class

## What Happens In This EDA

In the notebook, the dataset is first loaded and explored using:
- shape and data type inspection
- column checks
- descriptive statistics
- overview of categorical and numerical columns

Then several cleaning and preprocessing steps are done:
- the `id` column is dropped
- column names are renamed into simpler readable names
- `packed_cell_volume`, `white_blood_cell_count`, and `red_blood_cell_count` are converted to numeric
- inconsistent string values are cleaned in columns like `diabetes_mellitus`, `coronary_artery_disease`, and `class`
- the target `class` is mapped from `ckd` and `notckd` to numeric values
- missing values are handled later using median for numeric columns and mode for categorical columns

After that, the notebook explores patterns through different visualizations, including:
- age distribution
- hypertension countplot
- blood urea by CKD class
- serum creatinine by CKD class
- anemia countplot
- pus cell clumps countplot
- white blood cell count distribution
- coronary artery disease countplot
- pedal edema countplot
- bacteria countplot
- age vs blood pressure scatterplots
- diabetes mellitus vs albumin plots
- pairplot and pairgrid for selected clinical variables
- correlation heatmaps
- swarmplot for diabetes, age, and hypertension
- interactive Plotly scatterplots and 3D plots

The notebook also starts machine learning preparation by separating features and target:
- `X = df.drop('class', axis=1)`
- `y = df['class']`

## Purpose

The main purpose of this EDA is to understand how different clinical measurements and health conditions are related to Chronic Kidney Disease.

This project helps answer questions like:
- which medical variables show clearer differences between CKD and non-CKD cases
- how features like blood urea, creatinine, and haemoglobin behave across the dataset
- how related conditions such as hypertension, diabetes, anemia, and pedal edema appear in the data
- which variables may be useful for future CKD prediction models

## Files

- `3. EDA cronic data analysis.ipynb` : Jupyter notebook with the full EDA
- `kidney_disease.csv` : dataset used in the analysis
