# health-insurance-charges-prediction
"TechCrush Capstone  Predicting medical insurance charges using regression"

Predicting Medical Insurance Charges
Team Datawise | TechCrush Cohort 7; Data Science Capstone | Group 8 | Case Study 1: Healthcare
Team leader: Israel Humphrey

Problem Statement
Health insurers price policies based on personal and health-related risk factors, but it's often unclear which factors matter most and whether some factors compound each other. This project uses a real-world dataset of insured individuals to identify the key drivers of medical insurance charges and build a model that predicts those charges accurately.

Objectives
1. Explore relationships between personal/health attributes and insurance charges. 
2. Build a regression model to predict charges from these attributes. 
3. Diagnose and improve the model's prediction accuracy. 
4. Deliver business-relevant insights for risk assessment. 

Dataset
1. Source: Medical Cost Personal Dataset (insurance.csv). 
2. Size: 1,338 records (1,337 after removing 1 duplicate), 7 features. 
3. Features: age, sex, bmi, children, smoker, region, charges (target variable). 
4. No missing values. 

Methodology
1. Explore (EDA): Cleaned the data and examined relationships between age, BMI, smoking status, region, and charges. 
2. Model: Encoded categorical variables (One-Hot Encoding) and trained a Linear Regression model on an 80/20 train-test     split. 
3. Diagnose: Investigated individual prediction errors to find where the model performed poorly. 
4. Improve: Added a smoker × BMI interaction term to capture a compounding effect the original model missed. 

Key Findings
1. Smoking status is the single strongest predictor of charges — smokers pay ~4x more than non-smokers on average
   ($32,050 vs $8,434).
2.BMI alone has minimal effect, but combined with smoking, it nearly doubles charges further (obese smokers: $41,558 vs    non-obese smokers: $21,363). 
3. Age contributes a steady, moderate increase in charges. 
4. Sex, region, and number of children have minimal influence on charges. 

Model Results
Metric      Initial Model    Improved Model (with interaction term)
R² Score       0.81                 0.89
MAE           $4,177               $2,829
RMSE          $5,956               $4,573
Adding the smoker × BMI interaction term significantly improved accuracy, particularly for high-cost obese smokers  one individual's prediction error dropped from $8,065 to just $332.

Tech Stack
1. Python. 
2. pandas, numpy. 
3. matplotlib, seaborn. 
4. cikit-learn (LinearRegression, train_test_split, metrics). 
5. Jupyter Notebook. 

Repository Contents
1. Insurance_Charges_Prediction.ipynb — Full analysis: EDA, model building, diagnosis, improvement, and visualizations. 
2. insurance.csv Dataset used for the analysis. 

Team
Team Datawise  Group 8, TechCrush Cohort 7 Data Science Capstone. 

License
This project is for educational purposes as part of the TechCrush Data Science Capstone.

## Live Demo

Try the deployed prediction app here: [Insurance Charges Predictor](https://insurance-charges-app-8uelkxxgrtpsmwfpzujjrj.streamlit.app)

Enter a person's age, sex, BMI, children, smoker status, and region to get an instant estimated insurance charge.
