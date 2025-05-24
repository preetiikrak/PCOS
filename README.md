# PCOS Prediction Using Random Forest Classifier

This project analyzes clinical data related to Polycystic Ovary Syndrome (PCOS) and builds a machine learning model to predict PCOS status based on various clinical and biochemical features.

---

## Project Overview

PCOS is a common endocrine disorder affecting women of reproductive age. This project merges multiple clinical datasets, performs exploratory data analysis (EDA), cleans and preprocesses the data, and trains a Random Forest classifier to predict whether a patient has PCOS.

---

## Dataset

- **PCOS_data_without_infertility.xlsx** (Sheet: Full_new): Contains clinical and biochemical data excluding infertility information.
- **PCOS_infertility.csv**: Contains infertility-related data.

These datasets are merged on the common column `Patient File No.`.

---

## Features

The dataset contains multiple numeric and categorical features including:

- Demographic features: Age, Weight, BMI, Height, Marriage Status (Years), etc.
- Clinical measurements: Blood pressure, Pulse rate, Follicle counts, Endometrium thickness, Hormone levels (FSH, LH, AMH, TSH, etc.)
- Lifestyle indicators: Fast food consumption, Exercise habits, Skin and hair conditions.
- Target variable: `PCOS (Y/N)` indicating PCOS diagnosis.

---

## Methodology

1. **Data Import & Merge**  
   Data from Excel and CSV files are merged and cleaned (removing duplicates, handling missing values).

2. **Data Cleaning & Preprocessing**  
   - Convert string-numeric columns to numeric types.
   - Fill missing values with median values.
   - Remove outliers based on domain knowledge thresholds.

3. **Exploratory Data Analysis (EDA)**  
   - Descriptive statistics.
   - Correlation analysis with heatmaps.
   - Visualization of important features and their distribution across PCOS and non-PCOS groups.

4. **Feature Selection**  
   Dropping irrelevant columns and selecting features for the model.

5. **Model Training**  
   - Splitting dataset into train and test sets (70-30 split).
   - Training a Random Forest Classifier.
   - Hyperparameter tuning using GridSearchCV for optimal model parameters.

6. **Evaluation**  
   - Accuracy score.
   - Classification report (precision, recall, f1-score).
   - Confusion matrix visualization.
