# 🏥 Medical Insurance Charges Prediction — Data Cleaning & Feature Engineering

## 📌 Project Overview

This project focuses on preparing a real-world healthcare insurance dataset for Machine Learning modeling.
The main objective is to analyze how personal attributes such as age, BMI, smoking habits, and region affect medical insurance charges and to transform raw data into a model-ready dataset.

The project demonstrates a complete **data preprocessing pipeline** including Exploratory Data Analysis (EDA), Data Cleaning, Feature Engineering, and Feature Selection.

---

## 📂 Dataset

**Dataset:** Medical Cost Personal Dataset (insurance.csv)

The dataset contains information about:

* Age of the person
* Gender
* BMI (Body Mass Index)
* Number of children/dependents
* Smoking habits
* Residential region
* Annual medical insurance charges (target variable)

---

## 🔍 Exploratory Data Analysis (EDA)

Performed detailed analysis to understand the structure and behavior of the dataset:

* Checked dataset shape, data types, and summary statistics
* Verified missing values
* Analyzed distribution of medical charges
* Identified right-skewed distribution in charges
* Compared insurance cost across smokers and non-smokers
* Visualized relationships using histograms, boxplots, and countplots

**Key Observation:**
Smokers have significantly higher medical insurance costs compared to non-smokers.

---

## 🧹 Data Cleaning

The dataset originally contained categorical (text) values.
To make the dataset suitable for Machine Learning models, the following cleaning steps were performed:

* Converted `sex` → binary column `is_female`
* Converted `smoker` → binary column `is_smoker`
* Removed redundant text columns
* Applied one-hot encoding to the `region` column
* Verified that the dataset contains no null values

---

## ⚙️ Feature Engineering

New meaningful features were created to improve model understanding:

### BMI Category Creation

BMI values were converted into medical categories:

* Underweight
* Normal
* Overweight
* Obese

This helps the model understand health risk levels instead of just raw BMI numbers.

### Charges Binning

Insurance charges were grouped into:

* Low
* Medium
* High

This was required for statistical feature selection.

---

## 📊 Feature Selection (Chi-Square Test)

A **Chi-Square Test of Independence** was applied to identify which categorical features significantly affect insurance charges.

Decision rule:

* p-value < 0.05 → Important feature (kept)
* p-value ≥ 0.05 → Not important (removed)

**Result:**
The `smoker` feature was found to be the most influential factor affecting insurance charges.

---

## 📦 Final Output

The final dataset:

* Contains only numerical features
* Is free from missing values
* Is encoded and normalized for ML models
* Is ready for model training (Linear Regression, Random Forest, etc.)

Output file: `insurance_final.csv`

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy (Chi-Square Test)

---

## 🎯 Learning Outcomes

Through this project I learned:

* Real-world dataset preprocessing
* Statistical feature selection
* Handling categorical data
* Feature engineering techniques
* Preparing data for Machine Learning pipelines

---

## 🚀 Future Work

* Train regression models to predict medical insurance charges
* Compare model performance (Linear Regression, Random Forest, XGBoost)
* Deploy as a web application using Flask/React

---


