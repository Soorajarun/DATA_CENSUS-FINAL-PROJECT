CENSUS-DATA-PREDICTION

This analysis focuses on the Census Income Dataset, where the income variable is the target. The goal is to predict whether an individual’s annual income exceeds $50,000 based on demographic and employment attributes.

Dataset Overview Target Variable: Income Data Size: 32,561 rows and 15 columns. Missing Values: Missing values are represented by ? in the dataset.

Missing values (?) were replaced with NaN. Imputation techniques were applied to handle the missing values effectively.

Finding Duplicates: Identified and removed 24 duplicate records using the drop_duplicates() function. Outlier Detection and Handling:

Detected outliers in numerical features using the (IQR) method. Outliers were capped within the acceptable range based on lower and upper bounds.

Exploratory Data Analysis (EDA):

Visualizations were created to analyze feature distributions, relationships between variables

Feature Engineering Target Variable (y):

The target variable income is categorical. Converted into numeric using Label Encoding: <=50K as 0 and >50K as 1.

Features (X):

X contains several categorical variables (e.g., workclass, education, occupation). Converted categorical variables into numerical values using One-Hot Encoding.

Feature Selection Applied Random Forest Classifier for feature selection to identify the most important predictors of income. Extracted feature importance scores, ranked the features, and selected the top features contributing significantly to the model's accuracy. In this analysis, 8 training models were used for performance evaluation. The models are:

Logistic Regression Decision Tree Classifier Random Forest Classifier Gradient Boosting Classifier Support Vector Classifier (SVC) AdaBoost Classifier K-Nearest Neighbors (KNN) Classifier Bagging Classifier

After evaluating the models using metrics such as Accuracy, Precision, Recall, and F1 Score, the Gradient Boosting Classifier emerged as the best-performing model based on its highest accuracy score.

Further analysis was conducted on the Gradient Boosting Classifier to generate:

Classification Report: A detailed breakdown of the model’s performance for each class, including metrics like precision, recall, and F1 score. ROC Curve: A graphical representation of the model’s performance, showing the trade-off between the true positive rate (TPR) and the false positive rate (FPR). Additionally, a bar plot visualization was created to compare the accuracy of all the models, highlighting the Gradient Boosting Classifier as the best model. Hyperparameter tuning is used to improve model performance. A pipeline is created based on the best model to predict future data. The pipeline includes 12 features, and the unseen data from the file Income_unseen_data.csv is used for prediction." the result of unseen data prediction done by .71 accuracy In this project, we developed and evaluated a machine learning pipeline to predict income categories (<=50K and >50K) based on demographic and professional features. The pipeline incorporated preprocessing, feature scaling, and model training, ensuring a streamlined and reproducible workflow. The model's predictions can help businesses or organizations in decision-making processes, such as targeted marketing, resource allocation, or policy planning.
