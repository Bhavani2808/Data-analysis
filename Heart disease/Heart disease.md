### Report on Heart Disease Analysis Project



#### 1. Introduction

The **Heart Disease Analysis** project aims to extract insights from a comprehensive dataset related to heart disease. This report presents the findings from the Exploratory Data Analysis (EDA) and the model evaluation.

#### 2. Data Exploration

The dataset consists of 303 rows and 14 columns, representing various factors related to heart disease. The EDA revealed the following key insights:

- **Gender Distribution:** The dataset is imbalanced, with more male than female participants.
- **Age Distribution:** The age of participants ranges primarily between 29 and 77 years, with a significant concentration in the 50-60 age range.
- **Target Variable:** Approximately 54% of participants have heart disease.

#### 3. Analysis Findings

- **Correlation Analysis:** The correlation heatmap indicated that features like `cp` (chest pain type), `thalach` (maximum heart rate), and `oldpeak` (ST depression) are significantly correlated with the target variable.
- **Sex and Heart Disease:** Males are more likely to have heart disease compared to females, as shown by the count plots.
- **Chest Pain Type:** `Typical angina` and `asymptomatic` chest pain types are more associated with heart disease.
- **Age and Heart Rate:** Older participants generally have lower maximum heart rates, and a lower heart rate is associated with a higher likelihood of heart disease.

#### 4. Model Performance

A Random Forest Classifier was used to predict the likelihood of heart disease. The model's performance was evaluated using several metrics:

- **Accuracy:** The model achieved an accuracy of approximately 85%.
- **Confusion Matrix:** The confusion matrix revealed that the model has a good balance of true positives and true negatives.
- **ROC-AUC Score:** The ROC-AUC score was 0.90, indicating strong predictive performance.

#### 5. Conclusion

The analysis highlighted several important factors that influence heart disease, such as chest pain type, maximum heart rate, and age. The model developed in this project provides a reliable method for predicting heart disease, which could be beneficial for early diagnosis and preventive measures.

