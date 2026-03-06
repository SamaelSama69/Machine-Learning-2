# EasyVisa -- Visa Approval Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.9-blue) ![Machine
Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-green)
![Status](https://img.shields.io/badge/Project-Completed-success)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

------------------------------------------------------------------------

# Project Overview

The **EasyVisa Machine Learning Project** focuses on predicting whether
a visa application will be **Certified or Denied** based on applicant
and employer attributes.

Immigration agencies process thousands of visa applications each year.
Manual review of these applications is time-consuming and can lead to
inconsistencies. This project applies **machine learning classification
techniques** to assist in identifying applications with a higher
probability of approval.

The solution analyzes historical visa application data and builds
predictive models capable of supporting immigration decision-making
through **data-driven insights**.

------------------------------------------------------------------------

# Business Problem

Organizations seeking foreign workers must submit visa applications
through immigration authorities. Each application must be evaluated to
ensure:

-   The job cannot be filled by a domestic worker
-   Wages meet prevailing standards
-   The candidate meets qualification requirements

With the rapid growth in applications, automated assistance through
**machine learning models** can significantly improve efficiency and
consistency in the decision process.

------------------------------------------------------------------------

# Project Objectives

The key objectives of this project are:

-   Perform **data exploration and preprocessing** on visa application
    data
-   Identify important factors influencing visa approval
-   Train and evaluate multiple **classification algorithms**
-   Optimize models through **hyperparameter tuning**
-   Compare models using standardized performance metrics
-   Select the most reliable model for prediction

------------------------------------------------------------------------

# Dataset Information

The dataset contains **25,480 visa applications** with attributes
describing both the applicant and the employer.

### Dataset Shape

25480 rows × 12 columns

### Features

  Feature                 Description
  ----------------------- ------------------------------------------------
  case_id                 Unique identifier for visa application
  continent               Continent of applicant
  education_of_employee   Education level of applicant
  has_job_experience      Whether the applicant has prior job experience
  requires_job_training   Whether job training is required
  no_of_employees         Number of employees in employer company
  yr_of_estab             Year employer company was established
  region_of_employment    Intended employment region
  prevailing_wage         Average wage offered
  unit_of_wage            Hourly / Weekly / Monthly / Yearly
  full_time_position      Whether the job is full-time
  case_status             Target variable (Certified / Denied)

------------------------------------------------------------------------

# Data Preprocessing

The following preprocessing steps were performed:

-   Handling incorrect values
-   Removing irrelevant columns (`case_id`)
-   Encoding categorical variables
-   Train--test data splitting
-   Feature preparation for machine learning models

### Dataset Split

  Dataset        Size
  -------------- --------
  Training Set   17,836
  Test Set       7,644

------------------------------------------------------------------------

# Machine Learning Models Implemented

Multiple classification algorithms were implemented and compared:

1.  Decision Tree
2.  Bagging Classifier
3.  Random Forest
4.  AdaBoost
5.  Gradient Boosting
6.  XGBoost
7.  Stacking Classifier

The stacking classifier combines the strengths of several ensemble
models to improve prediction reliability.

------------------------------------------------------------------------

# Model Evaluation Metrics

Models were evaluated using:

-   Accuracy
-   Precision
-   Recall
-   **F1 Score (Primary Metric)**

F1 score was selected because both error types are important:

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

------------------------------------------------------------------------

# Feature Importance Insights

Key variables influencing visa certification include:

1.  Education level of applicant
2.  Prevailing wage
3.  Prior job experience
4.  Company size
5.  Region of employment

------------------------------------------------------------------------

# Technologies Used

### Programming

-   Python

### Libraries

-   Pandas
-   NumPy
-   Scikit-learn
-   XGBoost
-   Matplotlib
-   Seaborn

### Environment

-   Jupyter Notebook
-   Google Colab

------------------------------------------------------------------------

# Future Improvements

Potential improvements for this project include:

-   Deploying the model using **Flask / FastAPI**
-   Building an **interactive dashboard**
-   Integrating **SHAP explainability**
-   Creating an **automated ML pipeline**
-   Deploying the model as a **web application**

------------------------------------------------------------------------

# Author

**Sham Solanki**\
Master's in Data Science -- Deakin University

------------------------------------------------------------------------

# License

This project is licensed under the **MIT License**.
