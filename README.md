# Project Report: Analysis of Bank Customer Data

## Project Description

This project involved the analysis of data concerning bank customers, encompassing various parameters such as the number of children, employment duration, age, education, marital status, gender, income type, debt status, total income, and loan purpose.

## Project Goal

The primary objective of this study was to identify relationships between various customer parameters and the probability of loan repayment on time. This analysis aimed to provide the bank with valuable insights to make more informed decisions regarding loan approvals and interest rates.

## Tools and Libraries

The following tools and libraries were utilized for this project:

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Sklearn

## Project Steps

### Step 1: Explore General Data Information

In this initial step:

- We imported the Pandas library to handle data manipulation.
- We read the data from a CSV file.

### Step 2: Data Preprocessing

Data preprocessing was a crucial stage in ensuring the quality and reliability of our analysis. This step involved:

- Handling missing values to prevent incomplete data from influencing our results.
- Addressing anomalous values that could distort our analysis.
- Adjusting data types for consistency and compatibility.
- Eliminating duplicate entries to maintain data integrity.
- Categorizing data for more meaningful insights.

### Step 3: Explore Data and Answer Questions

This step was dedicated to exploring the data and answering key questions related to loan repayment:

- Analyzing the relationship between the number of children and timely loan repayment.
- Investigating the influence of marital status on loan repayment.
- Assessing how income levels affect the probability of on-time loan repayment.
- Exploring the impact of different loan purposes on timely loan repayment.


## Possible Reasons for Data Gaps

Data gaps observed in the dataset can be attributed to various factors, including human error, technical issues during data transfer, or the omission of certain information by clients.

## Why Filling Missing Values with Medians Is the Best Solution for Scale Variables

Filling missing values with median values is the most suitable approach for scale variables due to its robustness. The median is not affected by extreme values, making it the preferred method for mitigating the impact of outliers on the dataset.

## General Conclusion

We carried out a primary analysis of the data, revealed a clear imbalance of classes, negative to positive - 4 to 1.

We pre-processed the data, filled in the gaps, made one_hot_encoding.

Before dealing with the imbalance, we had the following maximum performance with these hyperparameters:

Decision tree - F1 max: 0.569 at depth = 6

Random forest - F1 max: 0.605 at depth = 19, n_estimators = 47

Logistic regression - F1 = 0.335

To combat the imbalance, we used the upsampling and downsampling methods.

After using the upsampling method, we got the following results:

Decision tree - F1 max: 0.596 at depth = 5

Random forest - F1 max: 0.63 at depth = 9, n_estimators = 47

Logistic regression - F1 = 0.49

After using the downsampling method, we got the following results:

Decision tree - F1 max: 0.597 at depth = 5

Random forest - F1 max: 0.605 at depth = 5, n_estimators = 37

Logistic regression - F1 = 0.485

On testing, the models got f1 = 0.875 with n_estimators=47, max_depth=9
