# Machine Learning Project – End-to-End Data Analysis and Modeling

## Overview
This project presents a complete end-to-end Machine Learning workflow, developed within a Jupyter Notebook.  
The goal is to demonstrate practical skills in data analysis, preprocessing, feature engineering, model development, evaluation, and interpretation, following a structured and reproducible approach.

The notebook is designed to be readable, well-documented, and suitable both for technical audiences and for non-technical stakeholders interested in understanding the modeling decisions and results.

---

## Objectives
- Perform an exploratory data analysis (EDA) to understand the underlying structure of the dataset  
- Apply appropriate data cleaning and preprocessing techniques  
- Engineer and select relevant features  
- Train and evaluate Machine Learning models  
- Interpret results using both statistical and model-based metrics  
- Provide clear conclusions and possible next steps  

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
The project is organized as a single notebook with the following logical sections:

1. **Data Loading**
   - Dataset import and initial inspection
   - Overview of variables and data types

2. **Exploratory Data Analysis (EDA)**
   - Descriptive statistics
   - Data visualization
   - Identification of patterns, trends, and anomalies

3. **Data Preprocessing**
   - Handling missing values
   - Feature scaling and encoding
   - Train/validation split

4. **Modeling**
   - Model selection rationale
   - Training of baseline and/or advanced models
   - Hyperparameter tuning (when applicable)

5. **Evaluation**
   - Performance metrics
   - Model comparison
   - Error analysis

6. **Interpretability and Insights**
   - Feature importance and/or model explanations
   - Business or domain interpretation of results

7. **Conclusions**
   - Summary of findings
   - Limitations
   - Possible improvements and future work

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
