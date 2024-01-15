# HEALTH INSURANCE CROSS SELL PREDICTION

I have undertaken the project of predicting whether a customer would be interested in buying Vehicle Insurance. This will help our company plan its communication strategy to reach out to those customers and optimize its business model and revenue.

## Abstract

An insurance policy is an arrangement by which a company provides compensation for specified loss, damage, illness, or death in return for a premium. Factors like age, gender, region code, vehicle damage, vehicle age, annual premium, and policy sourcing channel influence customers' decisions. This data analysis and prediction with machine learning models aim to understand the reasons for customer interest in vehicle insurance.

## Problem Statement

As an Insurance company providing Health Insurance, we need a model to predict if our past year's policyholders will be interested in our Vehicle Insurance. Predicting customer interest will help us plan our communication strategy, optimize our business model, and increase revenue.

## Data Description

We have a dataset containing information about demographics, vehicles, and policy details of customers interested in vehicle insurance. The dataset comprises 381,109 data points with features like age, gender, region code, driving license status, previous insurance status, vehicle age, vehicle damage history, annual premium, policy sales channel, and customer vintage. The 'Response' feature indicates customer interest (1 for interested, 0 for not interested).

## Project Outline

### 1. Data Wrangling

After loading the dataset, I observed that it has 381,109 rows and 12 columns with no null values. I performed outlier treatment using quantile methods.

### 2. Normalization

Following outlier treatment, I noticed that numeric columns had different scales. I applied min-max scaling for feature normalization.

### 3. EDA (Exploratory Data Analysis)

I explored numerical features like Age, Policy_Sales_Channel, Region_Code, and Vintage. Age was categorized as young, middle, and old age. Policy sales channel and region code were also categorized. Insights included that young customers were less interested, and certain regions and channels had fewer interested customers. Customers with vehicle damage history had a higher interest, and their annual premium was higher.

### 4. Encoding Categorical Values

I used one-hot encoding to convert categorical columns (e.g., Gender, Previously_Insured, Vehicle_Age, Vehicle_Damage, Age_Group, Policy_Sales_Channel_Categorical, Region_Code_Categorical) into numerical values.

### 5. Feature Selection

I computed correlations between numeric features and evaluated feature importance using Mutual Information.

### 6. Model Fitting

I experimented with various classification algorithms, including Decision Tree, Gaussian Naive Bayes, AdaBoost Classifier, Bagging Classifier, LightGBM, and Logistic Regression.

### 7. Hyperparameter Tuning

I optimized models using techniques such as GridSearchCV, RandomizedSearchCV, and HalvingRandomizedSearchCV.

### 8. Metrics Evaluation

I evaluated models using metrics like Confusion Matrix, Accuracy, Precision, Recall, F1-Score, ROC-AUC Score, and Log Loss.

## Conclusion

Starting from data cleaning to hyperparameter tuning, I achieved accuracy scores ranging from 68% to 85% before tuning. After tuning, the best model achieved an accuracy of approximately 87%. Considering precision and recall due to class imbalance, we selected the model with an 85% accuracy.

# Challenges Faced

- Handling a large dataset.
- Long processing times for available hyperparameter tuning methods.
- Memory optimization during hyperparameter tuning.

