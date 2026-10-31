# SaaS Customer Churn Prediction — Optimized Deep Learning Classification

# Mini Project Overview

### General Details

**Date:** 12-09-2026

**Student Name:** Gautham VR

**Batch / Cohort:** April-October (Afternoon)

**Project Title:** SaaS Customer Churn Prediction Using Deep Learning

**Project Type:** Binary Classification

---

### Tools, Libraries & Frameworks Used

**Programming Language:** Python

**Data Manipulation & Analysis:** Pandas, NumPy

**Data Visualization:** Matplotlib, Seaborn

**Machine Learning:** Scikit-Learn (Logistic Regression, Stratified Cross-Validation, Model Evaluation)

**Deep Learning:** TensorFlow, Keras (Feedforward Neural Network / Multi-Layer Perceptron)

**Data Preprocessing:** Scikit-Learn Pipeline, ColumnTransformer, SimpleImputer, MinMaxScaler, OneHotEncoder

**Model Persistence:** Joblib, Keras Model Saving

**Environment / Tools:** Jupyter Notebook, VS Code, Git, GitHub

---

### Project Breakdown & Execution

**What I Worked On:**

Developed a SaaS Customer Churn Prediction system using customer account information, usage logs, and support-ticket records. The objective was to predict whether a customer account is likely to churn (Yes/No).

The project involved customer-level feature engineering, data quality assessment, exploratory data analysis, missing value handling, categorical encoding, numerical scaling, and model development.

A Feedforward Neural Network (MLP) with multiple hidden layers, ReLU activation, Batch Normalization, Dropout, and a Sigmoid output layer was implemented using TensorFlow/Keras.

The Deep Learning model was evaluated against a Balanced Logistic Regression baseline using Stratified 5-Fold Cross-Validation and Out-of-Fold predictions.

**What I Completed:**

* Data Loading & Data Quality Checking
* Data Inspection and Missing Value Analysis
* Data Cleaning and Feature Engineering
* Customer-level Usage Log Aggregation
* Customer-level Support Ticket Aggregation
* Exploratory Data Analysis (EDA)
* Missing Value Imputation
* Categorical Feature Encoding
* Numerical Feature Scaling
* Class Imbalance Handling using Balanced Class Weights
* Logistic Regression Model Development
* Deep Learning Model Development (MLP)
* Neural Network Regularization using Dropout and L2
* Batch Normalization
* Early Stopping and Learning Rate Reduction
* Stratified 5-Fold Cross-Validation
* Out-of-Fold Prediction Generation
* Probability Threshold Optimization
* Logistic Regression vs Deep Learning Comparison
* Model Evaluation using Accuracy, Precision, Recall, F1-Score, ROC-AUC and PR-AUC
* Confusion Matrix Analysis
* ROC and Precision-Recall Curve Visualization
* Feature Importance Analysis
* Final Model Selection
* Final Churn Prediction for 74 Customer Accounts
* Model and Preprocessing Pipeline Saving

---

### Challenges & Solutions

**Blocker / Challenge 1: The dataset contained imbalanced churn and non-churn classes.**

**How I Addressed It:**

Identified the class distribution and used balanced class weights during Logistic Regression and Neural Network training. Evaluated model performance using Precision, Recall, F1-Score, ROC-AUC, and PR-AUC instead of relying only on accuracy.

**Blocker / Challenge 2: Multiple customer data sources needed to be combined.**

**How I Addressed It:**

Performed data quality checks and integrated account master data, usage logs, and support-ticket information using `account_id`. Aggregated multiple usage and support records into customer-level features.

**Blocker / Challenge 3: Missing values and invalid login activity affected data preparation.**

**How I Addressed It:**

Investigated missing values across datasets, converted invalid negative login counts into missing values, and implemented median and most-frequent imputation through Scikit-Learn preprocessing pipelines.

**Blocker / Challenge 4: Deep Learning performance needed to be compared fairly against a traditional Machine Learning model.**

**How I Addressed It:**

Implemented a Feedforward Neural Network using TensorFlow/Keras and compared it with Balanced Logistic Regression using Stratified 5-Fold Cross-Validation and Out-of-Fold predictions.

**Blocker / Challenge 5: The Neural Network could overfit because of the relatively small labelled dataset.**

**How I Addressed It:**

Used Dropout, L2 regularization, Batch Normalization, Early Stopping, and ReduceLROnPlateau to improve training stability and reduce overfitting.

**Blocker / Challenge 6: Selecting the most suitable final model for churn prediction.**

**How I Addressed It:**

Compared the models using Out-of-Fold evaluation metrics and selected the model with the better F1-Score. Logistic Regression achieved better overall results than the Deep Learning MLP in this experiment and was selected for final predictions.

---

### Model Evaluation Results

| Evaluation Metric | Logistic Regression | Deep Learning MLP |
| ----------------- | ------------------: | ----------------: |
| Accuracy          |              65.08% |            60.33% |
| Precision         |              42.49% |            38.28% |
| Recall            |              69.49% |            67.80% |
| F1-Score          |              52.73% |            48.93% |
| ROC-AUC           |              71.66% |            64.95% |
| PR-AUC            |              51.42% |            40.51% |

**Final Selected Model:** Balanced Logistic Regression

**Evaluation Method:** Stratified 5-Fold Out-of-Fold Evaluation

**Final Predictions Generated:** 74 Customer Accounts

---

### Deliverables & Socials

**Project Outputs:**

* Engineered Customer Feature Dataset (`account_features.csv`)
* Final Churn Predictions (`final_predictions.csv`)
* Model Validation Metrics (`optimized_validation_metrics.json`)
* Classification Reports (`optimized_classification_reports.txt`)
* Confusion Matrix Visualization
* ROC Curve Visualization
* Precision-Recall Curve Visualization
* Trained Logistic Regression Model
* Trained Deep Learning Model
* Saved Preprocessing Pipeline
* Jupyter Notebook with Complete Workflow
