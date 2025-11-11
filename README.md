# Predicting-Stroke-Risk-Using-Machine-Learning
 About This Project

This repository contains the full implementation of “Predicting Stroke Risk Using Machine Learning on Clinical and Lifestyle Data.”
The project explores how demographic, behavioral, and medical features can be leveraged to identify patients at risk of stroke using advanced machine learning models.

Through comprehensive data cleaning, exploratory data analysis (EDA) , and feature engineering, the study identifies key predictors such as age, glucose level, hypertension, and heart disease.
Models including Logistic Regression, Random Forest, and XGBoost are trained to achieve interpretable and accurate predictions.

The project follows best practices in data preprocessing, class balancing using SMOTE, and model evaluation through precision, recall, F1-score, and ROC-AUC metrics.

This work supports the broader goal of early detection and prevention of strokes by providing a data-driven foundation for clinical decision support systems.

 Project Overview: 
This project aims to build a predictive model that estimates the likelihood of stroke occurrences among patients using a combination of clinical, demographic, and lifestyle features.  
The goal is to identify high-risk individuals early, enabling healthcare providers to intervene proactively and reduce stroke-related morbidity and mortality.

The analysis follows a complete data science workflow — from data preprocessing and exploratory data analysis (EDA) to feature engineering, model development, and evaluation.

Key Objectives
Explore the impact of clinical and lifestyle factors on stroke risk.  
Engineer and select the most significant features for prediction.  
Compare multiple machine learning models for accuracy and interpretability.  
Generate insights that can inform preventive healthcare decision-making.

Dataset Description: 
The dataset is sourced from Kaggle’s Healthcare Stroke Prediction Dataset (Fedesoriano, 2021), containing 5,110 patient records with 12 features.

| Variable | Type | Description |
|-----------|------|-------------|
| `gender` | Categorical | Male, Female, or Other |
| `age` | Numeric | Age of the patient |
| `hypertension` | Binary | 1 if patient has hypertension, 0 otherwise |
| `heart_disease` | Binary | 1 if patient has heart disease, 0 otherwise |
| `ever_married` | Categorical | Yes or No |
| `work_type` | Categorical | Type of employment (Private, Self-employed, Govt_job, etc.) |
| `Residence_type` | Categorical | Urban or Rural |
| `avg_glucose_level` | Numeric | Average glucose level in blood |
| `bmi` | Numeric | Body Mass Index |
| `smoking_status` | Categorical | Smoking habits (formerly smoked, never smoked, etc.) |
| `stroke` | Binary | Target variable (1 = stroke occurred, 0 = no stroke) |


Data Cleaning and Preprocessing:

Key preprocessing steps include:
Handling Missing Data: Imputed missing `bmi` values with median (~3.9%).  
Outlier Treatment:Winsorization applied to `avg_glucose_level` and `bmi`.  
Encoding Categorical Variables: Used one-hot encoding.  
Feature Scaling:Standardized continuous variables using z-score normalization.  
Addressing Class Imbalance: Applied SMOTE to balance the minority (stroke) class.  

Exploratory Data Analysis (EDA):

Stroke prevalence increases sharply after age 60.   Patients with high glucose levels, hypertension, or heart disease show higher stroke probability.  
Lifestyle variables like smoking status and work type exhibit clear associations.  
Correlation analysis reveals no multicollinearity (|r| < 0.8), confirming variable independence.

Visualizations include:
1. Age distribution by stroke occurrence  
2. Stroke prevalence across categorical variables  
3. Correlation heatmap of numerical features  

Model Development
Three machine learning models are implemented and compared:
Logistic Regression – interpretable baseline model  
Random Forest Classifier ensemble learning for improved accuracy  
XGBoost Classifier gradient boosting for optimal performance  

Evaluation Metrics:
Accuracy, Precision, Recall, F1-score, and ROC-AUC.

 Results Summary:
Age, glucose level, and hypertension emerge as strong predictors.  
Random Forest and XGBoost outperform Logistic Regression in accuracy and recall.  
No evidence of overfitting after cross-validation.  
The model provides interpretable insights for clinical decision support.

Repository Structure:

Predicting-Stroke-Risk-Using-Machine-Learning/
│
├── data/ # Raw and processed datasets
│ ├── healthcare-dataset-stroke-data.csv
│
├── notebooks/ # Jupyter notebooks for analysis
│ ├── 01_data_cleaning.ipynb
│ ├── 02_exploratory_analysis.ipynb
│ ├── 03_model_training.ipynb
│
├── figures/ # Visualizations from EDA
│ ├── figure1_age_distribution.png
│ ├── figure2_categorical_analysis.png
│ ├── figure3_correlation_heatmap.png
│
├── reports/
│ ├── Assignment_3.1_Data_Summary_Draft.pdf
│
├── README.md
└── requirements.txt

References
Fedesoriano. (2021). *Healthcare Stroke Prediction Dataset. Kaggle.  
[https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
World Health Organization. (2023). The top 10 causes of death. 
[https://www.who.int/news-room/fact-sheets/detail/the-top-10-causes-of-death](https://www.who.int/news-room/fact-sheets/detail/the-top-10-causes-of-death)

Maintained by Team 09 – MSDS Program, University of San Diego (2025) 
# For academic and research purposes only.

