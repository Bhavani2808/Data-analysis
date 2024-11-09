# FraudForce: Fraud Detection System

Hi everyone! I’m Balabhavani, and now I’ll be explaining the **FraudForce: Fraud Detection System** project, which is designed to detect fraudulent transactions in financial data.

---

## Objective
The primary goal of this project is to identify fraudulent transactions from a dataset containing both genuine and fraudulent financial transactions. Using machine learning techniques, the aim is to classify each transaction accurately as either legitimate or fraudulent.

## Problem Statement
Fraud detection is a critical task in financial systems due to fraudulent activities like payment fraud or account takeovers. These activities are relatively rare compared to legitimate transactions, creating a class imbalance in the data, which makes fraud detection a complex but vital task for financial institutions.

## Data
The dataset used in this project includes various features of financial transactions, such as:
- **Transaction Amount**
- **Merchant Group**
- **Shipping Address**
- **Gender**
- **Card Type**
- **Entry Mode**
- **...and more.**

Given the nature of fraud detection, the dataset has a significant class imbalance, with fraudulent transactions being fewer compared to legitimate ones.

---

## Data Preprocessing
The dataset undergoes several preprocessing steps to ensure its suitability for machine learning models:

1. **Handling Missing Values**
   - **Median Imputation** for numerical columns (e.g., Transaction Amount)
   - **Mode Imputation** for categorical columns (e.g., Gender, Merchant Group)

2. **Feature Engineering**
   - **Label Encoding** for categorical features such as Gender, Merchant Group, and Card Type
   - **Standard Scaling** for numerical features like Transaction Amount to standardize the data for better model performance

3. **Class Imbalance Handling**
   - **SMOTE (Synthetic Minority Over-sampling Technique)** was used to oversample the minority class (fraudulent transactions) to balance the dataset for model training.

---

## Model Building
For this project, two popular machine learning models were used:

1. **Logistic Regression** – A simple yet interpretable model often used for binary classification tasks.
2. **Random Forest Classifier** – A more complex model that handles class imbalances effectively, providing better predictive performance.

---

## Model Evaluation
To assess the performance of the models, the following evaluation metrics were used:

- **Accuracy**: Provides an overall sense of model performance.
- **Confusion Matrix**: Offers insights into:
  - **True Positives** (fraudulent transactions correctly classified)
  - **False Positives** (legitimate transactions misclassified as fraudulent)
  - **True Negatives** and **False Negatives**
- **AUC-ROC Score**: Evaluates the model’s ability to distinguish between legitimate and fraudulent transactions. A higher AUC indicates better model performance.
- **Classification Report**: Includes precision, recall, and F1-score, which are crucial for fraud detection, particularly in assessing the model's accuracy in identifying fraudulent transactions while avoiding misclassification.

---

## Hyperparameter Tuning
To enhance the performance of the Random Forest model, **GridSearchCV** was employed to tune hyperparameters, including:
- **Number of Estimators** (trees in the forest)
- **Maximum Depth** of each tree

This tuning process helps improve the model’s ability to handle overfitting and increases predictive accuracy.

---

## Results
The model demonstrated strong results, with a high **AUC-ROC score** indicating strong performance in distinguishing between fraudulent and legitimate transactions. Additionally, a good balance was achieved between precision and recall, ensuring that fraudulent transactions were accurately identified while minimizing false alarms.

---

## Final Step: Saving the Model
After selecting the best-performing model, it was saved using **joblib**. This allows for deployment in production environments without needing to retrain the model each time a prediction is required.

---

## Conclusion
The **FraudForce** system effectively detects fraudulent transactions by preprocessing the data, training machine learning models, and addressing class imbalance. This project demonstrates the critical role of fraud detection systems in reducing financial losses and mitigating fraud risks for organizations.

Thank you for your attention, and feel free to reach out with any questions!

---

### Dependencies
- **Python** (version)
- **pandas**
- **scikit-learn**
- **joblib**
- **numpy**

