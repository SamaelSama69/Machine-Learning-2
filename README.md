# EasyVisa -- Visa Approval Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.9-blue) ![Machine
Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-green)
![Status](https://img.shields.io/badge/Project-Completed-success)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

------------------------------------------------------------------------

# Problem Statement

Build a machine learning model that predicts whether a visa application
will be **certified or denied** based on applicant and employer
characteristics.

------------------------------------------------------------------------

# Project Overview

The **EasyVisa Machine Learning Project** focuses on predicting visa
application outcomes using classification models. Immigration agencies
process thousands of applications annually, making manual review slow
and inconsistent.

This project uses **machine learning algorithms and ensemble methods**
to analyze historical visa application data and provide **data‑driven
predictions** that can support immigration decision systems.

The system aims to:

-   Identify applications with a higher probability of approval
-   Reduce manual screening effort
-   Improve decision consistency
-   Provide insights into factors influencing visa approvals

------------------------------------------------------------------------

# Business Problem

Employers in the United States submit visa applications when hiring
foreign workers. These applications must ensure:

-   The job cannot be filled by a domestic worker
-   Wages meet prevailing labor standards
-   Applicants meet qualification requirements

As application volumes increase, predictive analytics can help
authorities **prioritize and evaluate cases more efficiently**.

------------------------------------------------------------------------

# Project Objectives

The objectives of this project include:

-   Performing **data preprocessing and exploration**
-   Identifying factors influencing visa approvals
-   Building multiple **classification models**
-   Performing **hyperparameter tuning**
-   Comparing models using evaluation metrics
-   Selecting the best model for prediction

------------------------------------------------------------------------

# Dataset Information

The dataset contains **25,480 visa applications** with attributes
describing applicants and employers.

### Dataset Shape

25480 rows × 12 columns

### Features

  Feature                 Description
  ----------------------- --------------------------------------------
  case_id                 Unique identifier for visa application
  continent               Applicant continent
  education_of_employee   Applicant education level
  has_job_experience      Whether the applicant has prior experience
  requires_job_training   Whether job training is required
  no_of_employees         Number of employees in employer company
  yr_of_estab             Employer company establishment year
  region_of_employment    Intended employment region
  prevailing_wage         Average wage offered
  unit_of_wage            Hourly / Weekly / Monthly / Yearly
  full_time_position      Whether the job is full-time
  case_status             Target variable (Certified / Denied)

------------------------------------------------------------------------

# Data Preprocessing

Steps performed:

-   Handling incorrect values
-   Removing irrelevant columns (`case_id`)
-   Encoding categorical variables
-   Feature preparation for modeling
-   Splitting dataset into training and testing sets

### Dataset Split

  Dataset        Size
  -------------- --------
  Training Set   17,836
  Test Set       7,644

------------------------------------------------------------------------

# Machine Learning Pipeline

The model development pipeline consists of:

1.  Data Cleaning
2.  Feature Encoding
3.  Train/Test Split
4.  Model Training
5.  Hyperparameter Tuning
6.  Model Evaluation
7.  Model Comparison
8.  Feature Importance Analysis
9.  Final Model Selection

------------------------------------------------------------------------

# Machine Learning Models Implemented

The following classification algorithms were implemented:

1.  Decision Tree
2.  Bagging Classifier
3.  Random Forest
4.  AdaBoost
5.  Gradient Boosting
6.  XGBoost
7.  Stacking Classifier

The **Stacking Classifier** combines predictions from multiple ensemble
models to improve performance.

------------------------------------------------------------------------

# Model Evaluation Metrics

Models were evaluated using:

-   Accuracy
-   Precision
-   Recall
-   **F1 Score (Primary Metric)**

F1 score was chosen because both types of prediction errors are
critical.

  Error Type       Impact
  ---------------- -----------------------------------
  False Positive   Approving an unsuitable candidate
  False Negative   Rejecting a qualified candidate

------------------------------------------------------------------------

# Model Performance Comparison

  --------------------------------------------------------------------------
  Model          Accuracy       Precision      Recall         F1 Score
  -------------- -------------- -------------- -------------- --------------
  Decision Tree  0.706          0.715          0.931          0.809
  (Tuned)                                                     

  Bagging        0.724          0.744          0.895          0.813
  Classifier                                                  

  Random Forest  0.738          0.755          0.889          0.820
  (Tuned)                                                     

  AdaBoost       0.734          0.757          0.885          0.816

  Gradient       0.745          0.772          0.876          0.821
  Boosting                                                    

  XGBoost        0.745          0.775          0.869          0.820
  (Tuned)                                                     

  **Stacking     **0.744**      **0.770**      **0.880**      **0.821**
  Classifier**                                                
  --------------------------------------------------------------------------

### Final Model

The **Stacking Classifier** produced the most balanced results across
evaluation metrics.

------------------------------------------------------------------------

# Feature Importance Insights

Important predictors influencing visa certification include:

1.  Education level
2.  Prevailing wage
3.  Prior job experience
4.  Company size
5.  Region of employment

These variables strongly affect the probability of visa approval.

------------------------------------------------------------------------

# Key Takeaways

• Ensemble models outperform single decision tree models.\
• Education level and prevailing wage are the strongest predictors.\
• Gradient Boosting, Random Forest, and XGBoost provide stable results.\
• The Stacking Classifier achieved the best balanced performance.

------------------------------------------------------------------------

# How to Run the Project

## 1 Clone the repository

git clone https://github.com/yourusername/EasyVisa-ML-Project.git

## 2 Navigate to the project directory

cd EasyVisa-ML-Project

## 3 Install dependencies

pip install -r requirements.txt

## 4 Run the notebook

Open:

notebooks/EasyVisa_Model.ipynb

------------------------------------------------------------------------

# Repository Structure

EasyVisa-ML-Project │ ├── data │ └── visa_dataset.csv │ ├── notebooks │
└── EasyVisa_Model.ipynb │ ├── reports │ └── EasyVisa_Project_Report.pdf
│ ├── README.md

------------------------------------------------------------------------

# Technologies Used

Programming: - Python

Libraries: - Pandas - NumPy - Scikit-learn - XGBoost - Matplotlib -
Seaborn

Environment: - Jupyter Notebook - Google Colab

------------------------------------------------------------------------

# Future Improvements

Possible future improvements:

-   Deploy model using **FastAPI or Flask**
-   Build an **interactive dashboard**
-   Add **SHAP model explainability**
-   Implement **automated ML pipelines**
-   Deploy model as a **web application**

------------------------------------------------------------------------

# Author

**Sham Solanki**\
Master's in Data Science -- Deakin University

------------------------------------------------------------------------

# License

This project is licensed under the **MIT License**.
