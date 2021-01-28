# Respondent-Group-Classification
This project was given as a part of an assessment for my unnamed Company interview.

## Objective: Classification of the respondents into their respective classes. 

## Dataset: The dataset was provided by the Company and the features in the dataset. The features are named randomly and hence, do not give any information about the dataset.
* No of features: 301
* No of observations: 18379

## Packages:
* Numpy, Pandas, Matplotlib, Seaborn, sklearn

## Preprocessing:
* **Null Values**: The features with more than 800 null values were eliminated. Considering the number of observations, 800 is a fair number. The features with less than 800 null value were dealt with separately. The parameters obtained while handling null values were used to transform the null values in the test set. The numerical features were imputed with their means, and the categorical features were imputed with the most frequest occurring values.
<br />

* **Feature Handling**: 'Respondent_id' was removed from the dataset as it does not assist in the predictive process. The 'Year' Feature was also removed as the entire dataset is recorded for a single year.
<br />

* **Encoding**: The categorical variables, 'month' and 'var9' were one-hot encoded.
<br />

* **Feature Scaling** : The numerical features were scaled by calculating features' z-scores. This was necessary to run algorithms like PCA and Logistic Regression.
<br />

* **Imbalanced Classes**: The dataset was heavily imbalanced. Group 1 contained a total of 14197 observations out of 18379. This would affect the performance of the training and thus, accuracy. SMOTE was used to oversample the remaining classes in order to solve this problem. As SMOTE creates synthetic records and does not just replicate existing records, bias is avoided to a good extent.
<br />

## Dimensionality Reduction: 
* As the number of features were large, it has to beneficial to reduce the no of dimensions of the dataset. Enter, the most famous dimensionality reduction algorithm, Principal Component Analysis. The 300 features were reduced to a mere 30 principal components. The PCA parameters obtained while transforming the training set was used to transform the test set as well, to avoid data leakage.
<br />

