# **Details About the Dataset**
 ***Census Income***

 Kohavi,Ron. (1996). Census Income. UCI Machine Learning Repository. https://doi.org/10.24432/C5GP7S.

Predict whether income exceeds $50K/yr based on census data.



This dataset is licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license.

This allows for the sharing and adaptation of the datasets for any purpose, provided that the appropriate credit is given.

---

Instances - 48842

Features - 14
---
#Dataset Information
1.   Numerical - 6
2.   Categorical - 8

So, Totally 13 features or Columns  are there in the dataset.


---
# Answering the Questions

**Which independent variables have missing data? How much?**
1.   workclass = 963
2.   occupation = 966
3.   native-country = 274

**In the predictor variables independent of all the other predictor variables?**

> No, they're dependent on each other. This is shown in pain plot in [Correlation](#Correlation)


**What are the data types? (Only numeric and categorical)**

> Data Types :int64(*6 columns*), object(*8 columns*)

**Are there missing values?**
> Yes, There are missing values in 3 columns. in 
-  workclass         2799
-  occupation        2809
-  native-country     857
 

**What are the likely distributions of the numeric variables?**

> Most numerical variable are not having the similar distribution, some are highly skewed, some are slightly like normal distribution 


**Which independent variables are useful to predict a target (dependent variable)? (Use at least three methods)**

1. capital-gain
2. capital-loss
3. Workclass
4. Fnlwgt
5. Age
6. Native-country

Do the training and test sets have the same data?
> Yes, most of the data are similar but the data points in training set are not included in train and validation data set.

**Which predictor variables are the most important?**

1. capital-gain
2. capital-loss
3. Workclass
4. Fnlwgt
5. Age
6. Native-country

**Do the ranges of the predictor variables make sense?**

> Yes, Census data are usually different and diverse than any other dataset. It also depends upon the data collection.

What are the distributions of the predictor variables?

1.   **Age** - It might resemble a normal distribution, the heavier tails suggest that the overall distribution of age in this dataset is not perfectly normal.
2.   **Fnlwgt** - The distribution is heavily right-skewed which means that the bulk of the data is concentrated on the left with a long tail stretching to the right. It seems like a Logarithamic distibution.
3.   **Education-num** - It is not a normal distribution but the variable is not continuous but categorical with an order.
4.   **Capital-gain** - This distribution is highly right-skewed with many outliers at the higher end.
5.   **Capital-loss** - It is similar to Capital gain but has high outliers
6.   **Hours-per-week** - The distribution bit similar like normal but not perfectly normal.



**Remove outliers and keep outliers (does if have an effect of the final predictive model)?**

>Yes, There is a small improvement in accuracy of 0.007 after removing the outliers in capital-gain and capital-loss

**Remove 1%, 5%, and 10% of your data randomly and impute the values back using at least 3 imputation methods. How well did the methods recover the missing values?  That is remove some data, check the % error on residuals for numeric data and check for bias and variance of the error.**

> --- Removing 1% of data ---
Mean Imputation MSE: 205.14885388028884
Median Imputation MSE: 207.37345334116128
KNN Imputation MSE: 217.68777736577667


> --- Removing 5% of data ---
Mean Imputation MSE: 411.2860260491621
Median Imputation MSE: 414.41992368827465
KNN Imputation MSE: 446.68436424620546

>--- Removing 10% of data ---
Mean Imputation MSE: 600.1457935823508
Median Imputation MSE: 603.3634103193325
KNN Imputation MSE: 640.4100670660991

#Refernces
1. Sckit learn offcial documentation
2. Refered Towards Data Science
3. Eli5 official documentation
4. Pandas Documentation
The algorithms were referred directly from the Sckit learn official documentation. Visualization was referred from the Machine Learning with scikit-learn Quick Start Guide and Towards Data Science (How do you check the quality of your regression model in Python?). The remaining code was written independently. Feature importance reference is taken from eli5 offical documnetation





