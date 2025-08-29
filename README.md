Customer Churn Prediction in the Telecom Sector (CRISP-DM)

Author: Akash Nikam (DBS – MSc Data Analytics)
Tools: Python (scikit-learn, XGBoost, imbalanced-learn), RapidMiner AutoModel

Project Overview

This project applies the CRISP-DM methodology to predict customer churn in the telecom sector.
The goal is to identify high-risk customers early, allowing retention teams to take proactive measures such as discounts or personalized offers.

The analysis combines:

Python machine learning models (Logistic Regression, Random Forest, XGBoost).

RapidMiner AutoModel (no-code AutoML benchmarking).

The project focuses on maximizing recall (catching as many churners as possible), since missing churners is more costly than false alarms.

Tech & Libraries

Python 3.x, Jupyter Notebook

pandas, numpy, scikit-learn

xgboost, imbalanced-learn (SMOTE)

matplotlib, seaborn

RapidMiner AutoModel

Install all dependencies:

pip install -r requirements.txt

Dataset

Source: Telco Customer Churn dataset

Rows: 7,032

Columns: 31 (21 boolean, 8 integer, 2 continuous)

Target variable: Churn (0 = Retained, 1 = Churned)

Key churn drivers identified:

MonthlyCharges

TotalCharges

Tenure

Contract type (month-to-month contracts churn more)

Repository Structure
Customer-Churn-Prediction-Telecom/
├── Final code.ipynb                   # Python ML workflow (prep → SMOTE → models → eval)
├── telco_churn_cleaned.csv            # Cleaned dataset
├── Rapidminer analysis.rmp            # RapidMiner AutoModel workflow
├── CA02_Nikam_Akash_20054691_applied_project_report.pdf
├── Customer Churn Prediction in the Telecom Sector.pptx
├── results/
│   ├── Data description.png           # Dataset info / schema
│   ├── Python results.png             # Classification reports
│   ├── Python ROC curve.png           # ROC curve comparison
│   └── Rapidminer overview.png        # AutoModel leaderboard
└── README.md

Models & Evaluation
 RapidMiner AutoModel

Tested: Logistic Regression, Random Forest, Gradient Boosted Trees, Deep Learning

Best AUC: Random Forest (0.844)

Limitation: Lower recall on churners

 Python Models

Logistic Regression

Random Forest

XGBoost

Train/Test Split: 80/20 stratified
SMOTE: Applied only to training set for class balancing

Key Results
Model	                   Accuracy	 Recall	 ROC-AUC
Logistic Regression	      74–75%	  0.64    0.80
Random Forest	            77%	      0.65	  0.81
XGBoost	                  76%	      0.67	  0.81
RapidMiner RF	            78.6%	    0.42	  0.844

XGBoost (Python) → Best balance of recall, precision, interpretability.

Feature importance: MonthlyCharges, TotalCharges, Tenure.

Business Impact

Weekly churn scoring → high-risk customers flagged.

Retention team can act with personalized offers/support.

Reduces revenue leakage and boosts customer lifetime value.

Future Work

Real-time scoring API (Flask/FastAPI).

SHAP explainability for business transparency.

Hybrid ensemble of Python + RapidMiner models.

Integration with CRM tools (Salesforce, HubSpot).

Academic Artefacts

Report: CA02_Nikam_Akash_20054691_applied_project_report.pdf

Slides: Customer Churn Prediction in the Telecom Sector.pptx

Contact

For queries or collaboration:
Akash Nikam – MSc Data Analytics, Dublin Business School
📧 aakashn3118@gmail.com
