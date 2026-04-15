# JPMorgan-Chase-Fraud-Detection
Final Project for Applied Machine Learning Course

FOR DATA GO TO: https://www.jpmorganchase.com/about/technology/research/ai/synthetic-data

Overview

This project focuses on building a machine learning model to detect fraudulent financial transactions using a large-scale synthetic dataset provided by JPMorgan. The goal is to identify high-risk transactions with an emphasis on maximizing fraud detection (recall) in an imbalanced dataset.

Dataset

- Size: 1M+ rows
- Type: Synthetic transactional data
- Target Variable: Fraud label (binary classification)
- Challenge: Highly imbalanced dataset (fraud is rare)

Data Preprocessing
- Data cleaning and handling missing values
- Feature engineering to extract meaningful transaction patterns
- Scaling and transformation where necessary

Modeling
- Baseline Model: Logistic Regression
- Advanced Model: XGBoost Classifier
- Hyperparameter Tuning: Bayesian Optimization using BayesSearchCV

Evaluation Strategy
- Focused on metrics suitable for imbalanced classification:
  - ROC-AUC
  - Precision
  - Recall

Model: Logistic Regression
- ROC-AUC: 0.6070
- Precision: 0.03
- Recall: 0.63

Model: XGBoost
- ROC-AUC: 0.6988
- Precision: 0.029
- Recall: 0.899

Key Insights
- Improved ROC-AUC from 0.6070 → 0.6988 over baseline
- Achieved high recall (0.899), capturing ~90% of fraudulent transactions
- Low precision reflects real-world class imbalance, prioritizing fraud detection over false positives

Key Takeaways
- In fraud detection, recall is more critical than precision to minimize missed fraud cases
- XGBoost significantly outperformed logistic regression in identifying complex patterns
- Bayesian hyperparameter tuning improved model performance efficiently

Tech Stack
- Programming: Python
- Libraries: Pandas, NumPy, Scikit-learn, XGBoost, Scikit-Optimize
- Techniques:
  - Classification Modeling
  - Feature Engineering
  - Hyperparameter Optimization
  - Imbalanced Data Handling
 
Business Impact

- This model demonstrates how machine learning can be applied in financial services to proactively detect fraudulent transactions, reduce financial losses, and improve risk management strategies.
