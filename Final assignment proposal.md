
## **Proposal**: Investigating the Impact of Serum Cholesterol, Dietary Cholesterol, and Lifestyle Factors on Heart Disease Risk: Identifying Key Predictors

Emina Ganibegović, Jan Mucha, Kyrylo Stadniuk

**Research Question**: How do serum and dietary cholesterol levels correlate with the risk of heart disease, and what role do lifestyle factors—such as sleep quality, diet, stress, and exercise—play in the development of heart disease? Among these factors, which is the strongest predictor of heart disease risk?

### Datasets
- https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset
- https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset
- https://ieee-dataport.org/open-access/heart-disease-dataset-comprehensive?fbclid=IwZXh0bgNhZW0CMTAAAR2aUnATrW-4cwijS9ZQVWiq_W73ZF_PLabpEAolU2iuGLjYaK7qALgNiR4_aem_J53_znS0_axEj3DGXvfqEw
- Some others, that might be found in the future.



## Work Plan

### Step 1: Data Cleaning and Preprocessing
The datasets mentioned look fairly clean, nonetheless, the following steps should be executed:
- Filter relevant variables in each dataset, focusing on serum cholesterol, dietary cholesterol intake, heart disease indicators, and other lifestyle factors (sleep, diet, stress levels, exercise).
- Handle missing values through imputation or removal, depending on the dataset and variable distributions.
- Standardize variables across datasets to ensure uniformity, especially in units of measurement (e.g., cholesterol levels).
- Identify and remove influential points (Cook's distance).
- Ensure the absence of multicollinearity (VIF)
- Try to merge datasets.

### Step 2: Exploratory Data Analysis (EDA)

- **Descriptive Statistics**: Calculate means, medians, and standard deviations of key variables to assess general trends.
- **Correlation Analysis**: Calculate the correlation matrix.
- **Plots**: Plot variables against each other. Use LDA  to visualize datasets.
- **Clustering**: Find clusters with unsupervised learning (KNN, K-means, DBSCAN, HDBSCAN, Mean Shift, or GMMs) to see if we can group entries based on some criteria (e.g., occupation). 
### Step 3: Statistical Testing
- Perform an ANOVA test to see the differences between groups within the dataset (e.g., smokers/non-smokers).

### Step 4: Statistical Modeling

This is essentially a binary classification task, so we will use logistic regression.
- Use logistic regression to predict the probability of heart disease based on lifestyle and cholesterol levels. 
- Train the best possible model.
- Select the most important features.
- Optionally: Try other models for binary classification (LDA, Decision Trees, Random Forests, or Gradient Boosted Models).

### Step 5: Evaluation of Model Performance and Predictor Importance

•	**Model Evaluation Metrics**: Use AUC-ROC, accuracy, and precision-recall curves to evaluate model performance.
•	**Feature Importance Analysis**: Find the most influential features with Permutation Feature Importance and Shrinkage.
•	Perform **Cross-Validation**.

### Step 6: Analyze Results
Utilizing the Feature Permutation Importance results and ANOVA results, conclude which factors are the most important.

### Potential Problems
1. **Confounding**: Lifestyle factors often interrelate, which may lead to confounding. 
2. **Data Quality Issues**: Self-reported data (e.g., dietary intake) usually are not accurate, which might introduce some noise.
3. **Unknown Influences**: Genetic factors and unmeasured environmental exposures may also influence heart disease risk. 
4. **Dataset Merging**: Merging of the datasets might be too problematic due to presence/absence of features in the datasets and differences in units. So, we might have to train different models and analyze datasets separately.
5. **Low-Quality Data**: Publicly available datasets are not always of the highest quality, which may pose challenges to our analysis.

