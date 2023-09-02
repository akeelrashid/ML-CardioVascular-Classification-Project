# ML-CardioVascular-Classification-Project
![220801-Tran-Hearts-2060-tease_mao5hx](https://github.com/akeelrashid/ML-CardioVascular-Classification-Project/assets/121357205/ce8377be-3435-466b-b374-df6df13a45a3)

This project aims to predict the 10-year risk of developing coronary heart disease (CHD) using the Cardiovascular Risk Prediction dataset. The dataset contains information on 3,390 individuals with 16 predictor variables and 1 target variable. The variables represent potential demographic, behavioral, and medical risk factors.

# Problem Statement
The dataset is from ongoing cardiovascular study on residents of the town of Framingham, Massachutts. The classification goal is to predict whether the patient has a 10-year risk of failure coronary heart disease(CHD). The dataset provides the patient's information . It includes over 4000 records and 15 attributes. Each attribute is a potental risk factor. There are both demographic, behavioral, and medical risk factor

# Project Summary
I was tasked with analyzing a dataset from a cardiovascular study in Framingham, Massachusetts, containing 3,390 rows and 17 features. While the dataset did not contain any duplicate values, it did have some missing data in certain features, though the percentage of missing values was small and manageable. The features provided valuable patient information, including age, education, gender, smoking status, and health-related data such as cholesterol levels, diabetes status, blood pressure, BMI, glucose levels, and heart rate. My objective was to build a model capable of predicting a patient's risk of developing Coronary Heart Disease in the next 10 years based on this information.

# Project Steps:

### 1. Data Preprocessing
   - Treated missing values by imputing them with medians or modes based on feature distributions.
   - Categorized features into categorical, discrete, and continuous.
   - Decided not to treat outliers, considering the health-related nature of the problem and the dataset's size.

### 2. Exploratory Data Analysis (EDA)
   - Conducted thorough EDA, including univariate, bivariate, and multivariate analyses.
   - Generated insights, such as gender and smoking prevalence, diabetes rates, hypertension prevalence, and age distributions.
   - Discovered correlations between features and their potential impact on CHD risk.

### 3. Feature Engineering
   - Performed label encoding for categorical features.
   - Introduced new features like pulse_pressure, smoking_status, and Diabetic_status.
   - Calculated the Variance Inflation Factor (VIF) to assess multicollinearity.
   - Selected essential features for further analysis.

### 4. Handling Imbalanced Data
   - Addressed the imbalance in the dataset using SMOTE (Synthetic Minority Over-sampling Technique).

### 5. Model Selection and Training
   - Split the data into training and testing sets.
   - Trained various machine learning models, including Logistic Regression, K-Nearest Neighbors, Random Forest, Naive Bayes, and XGBoost.
   - Evaluated models using accuracy, precision, recall, F1-score, and AUC metrics.
   - Tuned hyperparameters using GridSearchCV.
### 6. Model Conclusion
   - Among all models, the XGBoost model stood out as the best performer. After extensive hyperparameter tuning, the XGBoost model achieved an impressive accuracy of 99% on the training set and 94% on the test set.
   -  Key hyperparameters included 'gamma': 0, 'learning_rate': 0.1, 'max_depth': 5, and 'n_estimators': 300.
   -  The model correctly predicted 518 class 0 patients and 509 class 1 patients out of 1152 patients. There were 90 false negatives and 35 false positives.


