
# Harmful algal bloom events prediction: comparing machine learning and deep learning algorithms
This is my master's thesis project, where I endeavored to address a research gap based on previous literature in the field of Harmful Algal Bloom events prediction. In my research, I adopted several imputation methods and compared various linear regression algorithms to assess the feasibility of enhancing experimental efficiency.
 


## Table of contents
* [Problem Statement](#Problem-statement)
* [Research Questions](#Research-questions)
* [Dataset](#dataset)
* [Method](#method)
* [Implementation](#inplementation)
* [Conclusion](#findings-and-conclusion)

## Problem statement
Given the increasing prevalence of harmful algal bloom events (HABs) and their detrimental impact on coastal regions worldwide, the timely and accurate detection of these events has become of paramount importance. The advent of machine learning techniques has offered promising avenues for addressing this imperative need. However, few studies have addressed the issue of datasets with high sparsity in HABs prediction using machine learning techniques. The goal of this study is to determine whether the utilization of factual data can achieve comparable model performance in predicting HABs compared to imputed data using machine learning and deep learning algorithms, specifically when encountering datasets containing a large amount of missing values.

## Research questions
### Main Research Question
How to predict harmful algal bloom events in New York Harbor by using machine learning and deep learning algorithms with and without data imputations? 
### Supporting Questions 

SQ1: To what extent do machine learning and deep learning models perform differently with factual data and data undergone imputation with multiple techniques?

SQ2: Which are the most important water quality indicators that contribute to harmful algal bloom events in New York Harbor?

## Dataset
The study utilized a dataset from [New York Open Data](https://data.cityofnewyork.us/Environment/Harbor-Water-Quality/5uug-f49n), containing over 89,000 rows of water quality parameters.
	

## Method	
Two datasets were prepared: one with factual data and another with imputations, to answer the first sub-question, SQ1. A pipeline architecture was implemented for robust model development, including data preprocessing, hyperparameter tuning, and validation. The performance of different models, including RF (baseline), SVR, and ANN, was compared using evaluation metrics such as R2, RMSE, and MAE. Feature importance permutation and selection were performed to answer the second sub-question, SQ2.


![This flowchart shows steps from raw data to feature selection](./flowchart.png)

## Implementation
Project is created with:
* Python version: 3.10.11
* Scikit-learn version: 1.2.2
* Matplotlib version: 3.7.1
* Google Colab


## Findings and Conclusion
Domain Knowledge Enhancement: The utilization of domain knowledge enhanced the efficiency of HABs prediction.

Best Performing Model: SVR with median imputation achieved the highest R2 score of 0.859, RMSE score of 9.360, and MAE score of 5.737 after feature selection.

Impact of Data Imputations: Models using factual data showed comparable performance to those using imputation techniques.

Identified Important Parameters: Seventeen important water quality parameters, including fluorometers, pH, and dissolved oxygen (DO), were identified for predicting HABs in New York Harbor.

Promising Variables: Several novel predictors, such as fluorometers, nitrate/nitrite, and ammonium, emerged as promising variables for HABs prediction.

The study's findings have significant societal and scientific relevance, including facilitating early detection of pollution events, prioritizing water quality management, and improving our understanding of complex aquatic ecosystems through machine learning based water quality analysis.