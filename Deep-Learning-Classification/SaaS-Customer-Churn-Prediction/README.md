# SaaS Customer Churn Prediction Using Deep Learning

A machine learning and deep learning project designed to predict customer churn in SaaS (Software as a Service) businesses using customer account information, usage patterns, and support ticket data.

## Project Overview

Customer churn is one of the major challenges faced by SaaS companies. Losing customers can affect business revenue and long-term growth.

This project analyzes customer-related data and develops predictive models to identify customers who are likely to leave a SaaS service.

The project implements a Deep Learning model using a Multi-Layer Perceptron (MLP) and compares its performance with a Logistic Regression baseline.

## Objectives

* Analyze customer account information.
* Explore customer usage patterns.
* Analyze customer support ticket data.
* Perform data preprocessing and feature engineering.
* Build a Deep Learning classification model.
* Compare Deep Learning with Logistic Regression.
* Evaluate models using classification metrics.
* Predict churn probabilities for previously unlabeled customers.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow / Keras
* Jupyter Notebook

## Dataset Description

The project uses five CSV datasets:

| Dataset                | Description                                   |
| ---------------------- | --------------------------------------------- |
| account_master.csv     | Customer account information                  |
| usage_logs.csv         | Customer usage activity                       |
| support_tickets.csv    | Customer support ticket information           |
| churned_labeled.csv    | Historical customer churn labels              |
| churned_to_predict.csv | Customers whose churn status needs prediction |

**Note:** Raw datasets are not included in this public repository.

## Project Workflow

1. Data Loading
2. Data Exploration and Analysis
3. Data Cleaning
4. Missing Value Handling
5. Feature Engineering
6. Categorical Encoding
7. Feature Scaling
8. Model Development
9. Model Training and Validation
10. Model Evaluation
11. Customer Churn Prediction

## Models Implemented

### 1. Logistic Regression

A baseline machine learning classification model used for comparison.

### 2. Deep Learning – Multi-Layer Perceptron (MLP)

A feedforward neural network developed using TensorFlow/Keras with multiple hidden layers.

The model uses:

* ReLU activation
* Sigmoid output activation
* Dropout regularization
* Model validation and early stopping

## Model Evaluation

Models were evaluated using Stratified 5-Fold Out-of-Fold predictions.

| Metric    | Logistic Regression | Deep Learning (MLP) |
| --------- | ------------------: | ------------------: |
| Accuracy  |              65.08% |              60.33% |
| Precision |              42.49% |              38.28% |
| Recall    |              69.49% |              67.80% |
| F1-Score  |              52.73% |              48.93% |
| ROC-AUC   |              71.66% |              64.95% |
| PR-AUC    |              51.42% |              40.51% |

### Model Selection

Logistic Regression achieved better overall performance than the Deep Learning model on the evaluated metrics.

Therefore, Logistic Regression was selected for generating the final predictions for the 74 unlabeled customer accounts.

## Project Structure

```text
SaaS-Customer-Churn-Prediction/
│
├── README.md
├── PROJECT_OVERVIEW.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── Optimized_Customer_Churn_Deep_Learning.ipynb
│
├── data/
│   └── raw/
│
├── models/
│
└── outputs/
    ├── eda_overview.png
    ├── oof_confusion_matrices.png
    ├── oof_precision_recall_curves.png
    └── oof_roc_curves.png
```

## Installation

Clone the repository:

```bash
git clone https://github.com/itsgvr/Deep-Learning-Projects.git
```

Navigate to the project directory:

```bash
cd Deep-Learning-Projects/Deep-Learning-Classification/SaaS-Customer-Churn-Prediction
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

## How to Run

1. Open the project in VS Code or Jupyter Notebook.

2. Install the required dependencies.

3. Provide the required datasets in the appropriate data directory.

4. Open the notebook:

   `notebooks/Optimized_Customer_Churn_Deep_Learning.ipynb`

5. Run the notebook cells sequentially.

## Conclusion

This project demonstrates the application of machine learning and deep learning techniques for predicting customer churn in SaaS businesses.

Both Logistic Regression and a Multi-Layer Perceptron were implemented and evaluated. Based on the evaluation results, Logistic Regression achieved better performance and was selected for the final customer predictions.

The project provided practical experience in data preprocessing, feature engineering, model development, model evaluation, and customer churn prediction.

---

**Project Category:** Deep Learning – Classification
**Project Type:** Binary Classification
**Developed by:** Gautham VR

