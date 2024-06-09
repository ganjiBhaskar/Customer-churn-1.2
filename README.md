# Customer-churn-1.2

# Customer Churn Prediction for a Telecommunications Company

### Table of Contents
1. [Business Understanding](#business-understanding)
2. [Data Understanding](#data-understanding)
3. [Data Preparation and Engineering](#data-preparation-and-engineering)
4. [Model Building](#model-building)
5. [Model Evaluation](#model-evaluation)
6. [Conclusion and Recommendation](#conclusion-and-recommendation)
7. [Deployment](#deployment)

---

### Business Understanding

#### Problem Statement
Develop a predictive model to estimate the likelihood of customer churn for a telecommunications company. The model should consider various factors such as customer demographics, usage patterns, billing history, and customer service interactions.

#### Objective
Build a predictive model that accurately identifies customers likely to churn. This helps the telecommunication company implement targeted retention strategies to reduce churn rates, enhance customer satisfaction, and improve overall profitability.

---

### Data Understanding

#### Description
The dataset includes various columns representing customer demographics, usage patterns, billing history, and customer service interactions.

#### Initial Data Checks
- **Missing Values**: Checked for missing values and handled them appropriately.
- **Duplicated Records**: Ensured no duplicate records were present.
- **Data Types**: Verified and corrected data types for various columns, such as 'TotalCharges'.
- **Exploratory Data Analysis (EDA)**: Performed statistical summaries and visualizations to gain insights into the dataset.

---

### Data Preparation and Engineering

#### Exploratory Data Analysis
- Conducted statistical analysis on key numerical features like tenure, MonthlyCharges, and TotalCharges.
- Visualized distributions and relationships between variables using various plots.
- Performed hypothesis testing to understand the association between variables and churn.

#### Data Cleaning
- Handled missing values in the 'TotalCharges' column by replacing them with the median.
- Grouped related service columns into a single feature to reduce dimensionality.
- Transformed categorical variables into binary features for better modeling.

---

### Model Building

#### Data Splitting
- Split the dataset into training (75%) and testing (25%) sets.

#### Preprocessing
- Used StandardScaler to normalize numerical features.
- Applied OneHotEncoder for binary categorical features and OrdinalEncoder for multi-class categorical features.
- Created a preprocessing pipeline to ensure consistency and efficiency in data preparation.

#### Models Used
- Logistic Regression
- SGD Classification
- Decision Tree Classification
- K-Nearest Neighbors (KNN) Classification
- Support Vector Classifier (SVC)

---

### Model Evaluation

#### Evaluation Metrics
Each model's performance was evaluated using:
- **Accuracy**: The proportion of correctly classified instances.
- **F1 Score**: The harmonic mean of precision and recall.
- **Recall**: The proportion of actual positives correctly identified.
- **Precision**: The proportion of positive identifications that are actually correct.
- **Confusion Matrix**: A table showing true positive, true negative, false positive, and false negative predictions.
- **Classification Report**: Detailed metrics for each class, including precision, recall, and F1 score.

#### Results
- **Logistic Regression**
  - Accuracy: 0.806680881307747
  - Precision: 0.801310289965637
  - Recall: 0.806680881307747
  - F1 Score: 0.8034499262609079

- **SGD Classification**
  - Accuracy: 0.8024164889836531
  - Precision: 0.7957643357722071
  - Recall: 0.8024164889836531
  - F1 Score: 0.7982590003366955

- **Decision Tree Classification**
  - Accuracy: 0.8009950248756219
  - Precision: 0.8055930730873044
  - Recall: 0.8009950248756219
  - F1 Score: 0.8030414095431544

- **K-Nearest Neighbors (KNN) Classification**
  - Accuracy: 0.7846481876332623
  - Precision: 0.7860350084981806
  - Recall: 0.7846481876332623
  - F1 Score: 0.7853206108150412

- **Support Vector Classifier (SVC)**
  - Accuracy: 0.8109452736318408
  - Precision: 0.8020466500566307
  - Recall: 0.8109452736318408
  - F1 Score: 0.8043259116384892

---

### Conclusion and Recommendation

The SVC achieved the highest accuracy (81.1%) and balanced performance across other metrics. The Logistic Regression model also performed well with an accuracy of 80.7%. The Decision Tree Classifier had a slightly lower performance with an accuracy of 80.1%, while the KNN Classifier had the lowest performance among the evaluated models.

**Recommendation**: Based on the evaluation metrics, the SVC is recommended for deployment due to its high accuracy and balanced performance. The Logistic Regression model is a close second and can be considered as an alternative, especially if model interpretability is important.

---

### Deployment

A Streamlit application was developed to predict customer churn for a telecommunications company based on various input features. The application utilizes a trained machine learning model to make predictions.

#### Steps to Interact with the Application
1. **Input Features**: Provide necessary information about the customer demographics, usage patterns, billing history, and service interactions.
2. **Click on Predict**: After entering the required information, click on the "Predict" button.
3. **View Prediction**: The application will display whether the customer is likely to churn or not based on the provided input.

---



Customer churn
deployment link:-
https://customer-churn-12-by4vhwvhnoqeamdmk3kjbf.streamlit.app/
