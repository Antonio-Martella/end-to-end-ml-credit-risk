# Machine Learning Project – End-to-End Data Analysis and Modeling

## Overview
This project presents a complete end-to-end Machine Learning workflow. 
The goal is to demonstrate practical skills in data analysis, preprocessing, feature engineering, model development, evaluation, and interpretation, following a structured and reproducible approach.

The notebook is designed to be readable, well-documented, and suitable both for technical audiences and for non-technical stakeholders interested in understanding the modeling decisions and results.

---

## Objective of the Analysis

The objective of this project is to develop a model capable of estimating customer creditworthiness, with the aim of supporting decisions regarding credit card issuance. The model not only predicts whether an application will be approved or rejected, but also provides clear and interpretable reasons based on the customer's individual characteristics.

Specifically, it aims to:

* Identify the main factors that influence creditworthiness.

* Support automated decisions for credit card issuance, reducing risk and evaluation times.

* Provide transparent explanations for each decision, to justify any rejections or approvals.

This approach combines predictive accuracy with interpretability, making the decision-making process more robust and reliable.

---

## Dataset Description

The dataset contains information about customers who have applied for and obtained a credit card. Each record represents an individual applicant and includes demographic, financial, and behavioral attributes used to assess creditworthiness.

Main features include:
- **ID**: Unique customer identifier
- **CODE_GENDER**: Customer gender
- **FLAG_OWN_CAR**: Car ownership indicator
- **FLAG_OWN_REALTY**: Home ownership indicator
- **CNT_CHILDREN**: Number of children
- **AMT_INCOME_TOTAL**: Annual income
- **NAME_INCOME_TYPE**: Income category
- **NAME_EDUCATION_TYPE**: Education level
- **NAME_FAMILY_STATUS**: Marital status
- **NAME_HOUSING_TYPE**: Housing type
- **DAYS_BIRTH**: Days since birth
- **DAYS_EMPLOYED**: Days since employment start (positive values indicate unemployment duration)
- **FLAG_MOBIL / FLAG_WORK_PHONE / FLAG_PHONE / FLAG_EMAIL**: Contact availability indicators
- **OCCUPATION_TYPE**: Occupation category
- **CNT_FAM_MEMBERS**: Number of family members

The target variable (**TARGET**) is binary:
- **1**: Customer with high credit reliability (regular and consistent repayments)
- **0**: Customer with lower credit reliability


---

## Project Structure

The project is developed as a single, well-structured notebook and follows a complete Machine Learning workflow:

1. **Problem Definition**
   - Definition of the business objective: predicting customer creditworthiness for credit card approval
   - Framing the task as a binary classification problem with interpretability requirements

2. **Dataset Understanding**
   - Description of the dataset and target variable
   - Initial data inspection and validation
   - Identification of irrelevant or non-informative features

3. **Exploratory Data Analysis (EDA)**
   - Analysis of demographic, financial, and employment-related features
   - Study of feature distributions and class imbalance
   - Identification of meaningful relationships between features and the target
   - Handling of outliers and rare categories

4. **Feature Engineering**
   - Binning of high-variance discrete features (e.g. number of children, family size)
   - Log-transformation of skewed numerical variables (income)
   - Creation of derived features (age in years, employment duration, employment status)
   - Treatment of missing values using domain-driven assumptions

5. **Data Preprocessing**
   - Train/test split with class stratification
   - Scaling of numerical features
   - One-hot encoding of categorical variables
   - Construction of a preprocessing pipeline to prevent data leakage

6. **Modeling**
   - Training and comparison of multiple classification models:
     - Logistic Regression
     - Linear SVM
     - Random Forest
     - Gradient Boosting
     - Multilayer Perceptron (MLP)
   - Cross-validation-based evaluation using ROC-AUC, precision, and recall

7. **Model Selection and Hyperparameter Tuning**
   - Selection of the most promising model based on cross-validation results
   - Hyperparameter optimization using randomized search
   - Final model selection based on performance stability and generalization

8. **Performance Evaluation**
   - Evaluation on training and test sets
   - Analysis of ROC-AUC, classification metrics, and confusion matrix
   - Decision threshold optimization using Youden’s J statistic

9. **Model Explainability**
   - Global and local interpretability using SHAP values
   - Analysis of feature contributions to individual predictions
   - Generation of human-readable explanations to support decision transparency

10. **Conclusions**
    - Summary of results
    - Business interpretation of model behavior
    - Limitations and future improvements


---

## Used packages
- **Python**
- **NumPy**
- **Pandas**
- **Matplotlib / Seaborn**
- **Scikit-learn**
- *(Other libraries are listed directly inside the notebook)*

---

## How to Run the Notebook
1. Clone the repository:
   ```bash
   git clone https://github.com/Antonio-Martella/end-to-end-ml-credit-risk.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook

---

## Results
The final model (Random Forest) was trained with optimized hyperparameters and a tuned decision threshold to improve class-level performance.

The model shows excellent discriminative ability, with consistent performance between training and test data:
- Train ROC-AUC: 0.98
- Test ROC-AUC: 0.98

On the test set, the model achieves strong overall accuracy while maintaining high recall on the minority class:
- Accuracy: 0.96
- Class 1 (minority class):
  - Precision: 0.70
  - Recall: 1.00
  - F1-score: 0.82

The results indicate a well-generalizing model with a strong ability to identify positive instances, achieved through explicit decision threshold optimization. Detailed evaluation and error analysis are available in the notebook.


---

## Author

Antonio Martella, Machine Learning / Data Science Enthusiast :)

This project is part of a personal portfolio aimed at showcasing applied Machine Learning skills in real-world scenarios.

---

## Notes

This project is intended for educational and demonstrative purposes.
Feedback and suggestions are welcome.
