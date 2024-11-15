# Credit-Card-Fraud-Detection
This project applies machine learning techniques to detect fraudulent credit card transactions. By addressing the challenge of class imbalance in fraud detection, the project aims to build an accurate and interpretable model suitable for real-world applications.

# Overview
Fraud detection in credit card transactions is crucial for reducing financial losses. This project uses machine learning techniques to detect fraudulent transactions while balancing precision and recall to avoid inconveniencing legitimate customers.

# Project Goals
Accurately detect fraudulent transactions using machine learning.
Address class imbalance effectively to minimize false negatives and false positives.
Interpret the model’s decisions to ensure transparency and business relevance.
Provide actionable insights for deploying the model in real-world fraud detection systems.
# Dataset
The dataset contains credit card transactions from European cardholders in September 2013. 
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
# Features:
Time: Seconds elapsed between each transaction and the first transaction.
Amount: Transaction amount.
Class: Target variable where 1 indicates fraud and 0 indicates non-fraud.
28 anonymized features (V1 to V28) derived using PCA.
The dataset is highly imbalanced, with fraudulent transactions comprising only about 0.17% of the total.
# Methodology
# Data Exploration and Preprocessing:

Handled class imbalance using techniques like SMOTE.
Standardized features for consistency in model training.
Modeling:

Tested multiple models, including Logistic Regression, Decision Tree, Random Forest, and XGBoost.
Selected an ensemble of Random Forest and XGBoost for optimal performance.
Evaluation:

Evaluated models using metrics for imbalanced data (AUPRC, AUC-ROC, precision, and recall).
Used SHAP for feature importance to interpret the model’s key predictors of fraud.
Deployment Considerations:

Discussed strategies for regular retraining, threshold adjustment, and monitoring in a production setting.

# Results
Best Model: Ensemble of Random Forest and XGBoost.
Performance Metrics:
AUPRC: 0.88
AUC-ROC: 0.98
Precision (Fraud Class): 0.94
Recall (Fraud Class): 0.85
The ensemble model provides strong performance for fraud detection, balancing false positives and false negatives effectively.
Key Insights
Top Features for Fraud Detection:

SHAP analysis identified features V4, V14, V12, and V10 as the most significant predictors of fraud.
Business Impact:

The model’s high recall reduces missed fraud cases, helping to minimize financial losses.
High precision ensures fewer legitimate transactions are mistakenly flagged, improving customer experience.
Deployment Recommendations:

Regular Retraining to adapt to new fraud patterns.
Threshold Adjustment based on business priorities, either focusing on recall or precision.
Monitoring to track model performance over time.

# Requirements
Python 3.x
Jupyter Notebook
Required libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, shap, imblearn

# Conclusion
This project demonstrates an effective approach to credit card fraud detection using a machine learning ensemble model. With high precision and recall, the model balances fraud detection accuracy with customer experience, making it suitable for real-world deployment.
