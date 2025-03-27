# HSCT-Survival-Prediction

This project aims to predict the survival outcomes of Hematopoietic Stem Cell Transplantation (HSCT) patients using machine learning techniques. The workflow encompasses data preprocessing, exploratory data analysis (EDA), feature engineering, and model development to ensure robust and accurate predictions.

Data Preprocessing and EDA:

The workflow includes data preprocessing, exploratory data analysis (EDA), and visualization.
Importing essential libraries for:
•	Data Handling: pandas, numpy
•	Visualization: matplotlib, seaborn
•	Machine Learning: sklearn

The dataset was loaded using Pandas, and an initial preview was obtained using .head(), .shape, and .info() to understand the structure and characteristics of the dataset.

We have a dataset with dimensions of 28800 rows and 60 columns before preprocessing of the dataset.

Duplicate rows were identified and removed to ensure data quality.
Missing values were identified and handled appropriately, columns with high number of null values were analyzed for detailed understanding of the importance of the columns to predict the target variable. After removing the null values from each row, we have a dataset with 1974 rows and 60 columns for further analysis.

Exploratory Data Analysis

EDA was conducted to identify patterns and relationships within the dataset.

Plotted various plots like histogram and scatter plots to check the distribution of the features. Also used bar plots to check how each variable affects the survival chances and how long it takes if there is any chance of reoccurrence of the disease conditions or time for graft rejection i.e., event free survival time.

Observing how graft type has affected the efs time for different patients and how it is getting affected with related to the  age of the donor and age of the recipient at the time of the haemopoietic cell transplantation.

Feature Engineering

For further analysis we converted all the categorical values to numerical values tried using both encoding techniques label encoding and one hot encoding, Our goal is to predict the feature importances for Selected the most relevant features based on correlation and domain knowledge which has great effect on the target variable and choosing it for further analysis.

UPGRADES

I have also used boxplot visualization to find out the outliers, and then concatinated both categorical and numerical features and used RobustScaler that is robust to outliers and would perform better than standard scaler in case of outliers. I utilized PCA dimensionality technique to reduce the dimensions and calculate number of features to retain 95% variance.

I have used the PCA scaled data to fit the Random Forest Classifier and plotted a graph to select out the important features using feature selection in descending order. Also used Decision Tree Classifier to check its performance and how much it differs from Random Forest


Recent Upgrades:

Earlier to fit the Random Forest Classifier I used X_scaled instead of PCA scaled data, which automatically filtered the dataset to 28 features.


### Other Models

I have added other models like the ensemble methods - boosting techniques say Adaboost and gradient boosting classifier to predict the event free survival, gradient boosting performed better than Rando forest, while the Adaboost reached a 90% accuracy.

*** Placed Adaboosting and gradient boosting side by side for better clarification


** Utilised Shap to extract how each feature is contributing to the final outcome, It displays a clear output of each feature.

** Added Shap at three different positions- before standardizing the data, after standardization, and after dimensionality reduction on XGBOOST Classifier Model.






