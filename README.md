# Master_Thesis_2023
**Problem Statement:**
Given the increasing prevalence of harmful algal bloom events (HABs) and their detrimental impact on coastal regions worldwide, the timely and accurate detection of these events has become of paramount importance. The advent of machine learning techniques has offered promising avenues for addressing this imperative need. However, few studies have addressed the issue of datasets with high sparsity in HABs prediction using machine learning techniques. The goal of this study is to determine whether the utilization of factual data can achieve comparable model performance in predicting HABs compared to imputed data using machine learning and deep learning algorithms, specifically when encountering datasets containing a large amount of missing values.

Research Questions:

Main Research Question: How to predict harmful algal bloom events in New York Harbor by using machine learning and deep learning algorithms with and without data imputations?
Supporting Questions:

SQ1: To what extent do machine learning and deep learning models perform differently with factual data and data undergone imputation with multiple techniques?

SQ2: Which are the most important water quality indicators that contribute to harmful algal bloom events in New York Harbor?

**Approach:**
The study utilized a dataset from New York Open Data, containing over 89,000 rows of water quality parameters. Two datasets were prepared: one with factual data and another with imputations, to answer the first sub-question, SQ1. A pipeline architecture was implemented for robust model development, including data preprocessing, hyperparameter tuning, and validation. The performance of different models, including RF (baseline), SVR, and ANN, was compared using evaluation metrics such as R2, RMSE, and MAE. Feature importance permutation and selection were performed to answer the second sub-question, SQ2.


**Challenges, Limitations, and Future Directions:**

The research encountered several challenges and limitations that warrant consideration for future studies and improvements:

**Challenges and Limitations:**

1. **Outliers Handling**: The presence of potential outliers in the data presented a challenge. Due to the lack of extensive domain knowledge, it was difficult to determine whether extreme data points were genuine outliers or linked to influential events.

2. **Missing Crucial Features**: Certain essential features, such as COD, known as critical predictors in previous studies, were unavailable in the dataset. Additionally, the possibility of utilizing BOD instead of BOD5 to predict HABs in New York Harbor was not explored.

3. **Small Sample Size**: The sample size after filtering was relatively small, comprising fewer than 2000 samples, which may have implications on the model's generalizability.

4. **Handling Covariant Features**: The method employed for eliminating highly covariant features was effective primarily for variables exhibiting linear correlations, potentially overlooking non-linear relations among the features.

5. **Limited Hyperparameter Tuning**: The tuned ANN model had identical hyperparameters across all imputation methods, and the limited search range for hyperparameters may have influenced the model's performance.

6. **Missing Data Mechanisms**: The study did not conduct an analysis of missing data mechanisms, such as missing completely at random (MCAR), missing at random (MAR), and missing not at random (MNAR), which can impact the suitability of the chosen methods for imputation.

7. **Adequacy of Imputation Techniques**: The employed imputation techniques may not be adequate for addressing datasets with more than 70% missingness, and median imputation exhibited higher standard error, indicating greater uncertainty in predictions.

**Future Directions:**

1. **Expert Collaboration**: Collaborating with domain experts can aid in effectively handling outliers and gaining deeper insights into their significance.

2. **Utilizing BOD**: Exploring the use of BOD instead of BOD5 as one of the predictors for HABs in New York Harbor could provide new insights in this field.

3. **Non-linear Relations**: Adopting alternative techniques, such as partial dependence plots, to capture non-linear relations among the features can help identify more highly correlated features.

4. **Missing Data Mechanisms Analysis**: Understanding the missing data mechanisms in the dataset before deciding on the appropriate approach (complete case analysis or imputation) can lead to more robust modeling.

5. **Hyperparameter Tuning**: Expanding the range of randomized grid search for hyperparameters can potentially improve model performance.

6. **Advanced Imputation Techniques**: When imputation becomes necessary, advanced methods like deep matrix factorization (DMF) can be employed to address datasets with high levels of missing data and reduce uncertainty associated with median imputation.

Addressing these challenges and incorporating future directions can enhance the robustness and effectiveness of HABs prediction models, contributing to better water quality management and ecological preservation in coastal regions.

**Key Findings:**

1. **Domain Knowledge Enhancement**: The utilization of domain knowledge enhanced the efficiency of HABs prediction.

2. **Best Performing Model**: SVR with median imputation achieved the highest R2 score of 0.859, RMSE score of 9.360, and MAE score of 5.737 after feature selection.

3. **Impact of Data Imputations**: Models using factual data showed comparable performance to those using imputation techniques.

4. **Identified Important Parameters**: Seventeen important water quality parameters, including fluorometers, pH, and dissolved oxygen (DO), were identified for predicting HABs in New York Harbor.

5. **Promising Variables**: Several novel predictors, such as fluorometers, nitrate/nitrite, and ammonium, emerged as promising variables for HABs prediction.


The study's findings have significant societal and scientific relevance, including facilitating early detection of pollution events, prioritizing water quality management, and improving our understanding of complex aquatic ecosystems through machine learning-based water quality analysis.
