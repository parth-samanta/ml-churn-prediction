# ml-churn-prediction
Customer churn prediction using preprocessing, feature engineering, and ML modeling

#  Churn Prediction – Binary Classification 


The goal is to develop a machine learning model that predicts whether a customer will **churn (1)** or **not churn (0)** using structured customer data containing both **numerical and categorical features**.

---

## Objective

> Predict a binary target variable (`Churn`) using a variety of customer-related features.  
> Build a model with strong generalization ability 

---

##  Approach

The notebook `churn_predictor` contains the following workflow:

### 1️ Exploratory Data Analysis (EDA)
- Dataset overview (shape, dtypes, class balance)
- Correlation analysis  
- Feature distributions  
- Missing value inspection  

### 2️ Data Preprocessing
- Imputation for missing values  
- Encoding categorical variables (`OneHotEncoder`)  
- Feature scaling (`StandardScaler` / `MinMaxScaler`, if required)  
- Train-validation split (`random_state=42`)  

### 3️ Model Training & Evaluation
- Tested baseline ML models:
  - Logistic Regression  
  - Decision Tree / Random Forest  
  - Gradient Boosting (XGBoost / LightGBM, if used)  
- Cross-validation (`StratifiedKFold`)  
- Evaluation metrics:
  - Accuracy
  - Precision, Recall
  - **F1-score (primary metric)**

---

##  Final Results

| Metric | Score |
|-------|-------|
| **F1 Score (Validation)** | **0.65930** |


---

## Repository Structure

```text
.
├── churn_predictor.ipynb     # Main notebook (full pipeline)
├── data/
│   ├── train.csv             # Training data (not pushed to GitHub)
│   └── test.csv              # Test data (if provided)
├── submissions/
│   └── submission.csv        # Final Kaggle submission file
└── README.md                 # Project documentation
