# ML-CardioVascular-Classification-Project
# Project Summary
I have been given a data-set of cardiovascular study on residents of the town of Framingham, Massachusetts.The dataset contains 3390 rows and 17 features.The dataset doesn't contains any duplicate values but there are many features that contains null values but the percentage of null values is very small and it can be adjusted.The features in the datatset gives us information about the patient like what is the age,education,sex of patient and information like whether the patient is smoker or not if yes then how many cigrates he/she smokes per day and health related information whether the patient is taking any BPmed or not, what is his/her cholestrol level,is he/she diabetic or not,what is his/her BP,BMI,glucose level and heartrate.Using all this information I have to build a model that can predict what are the chances that the patient is at risk of developing Coronary Heart Disease in next 10 years.

First of all i treated all the null values present in my datatset with median/mode based on the distribution of that feature and then i distinguish all the features into categorical,discrete,and contionous and the data also contains some outliers but since it is a health related problem and we have small dataset also, so i am not going to treat the outliers as it might be containing some useful information

After cleaning the data i performed EDA (univeriate,Biveriate and Multiveriate analysis), in order to extract some useful insights from the data.Then i performed Feature Enginering and data preprocessing in which i performed label encoding for categirical features and defined some new features like pulse_pressure,smoking_status,and Diabetic_status and then i calculated VIF to find out Multicolinearity between the features and selected important feature for futher analysis.

Since the data is very imbalanced SMOTE(over-sampling) was used to deal with that

After spilliting the data in train and test ,i transformed the data using standard scaler and then i oversampled the data in order to balance it and then i implemented different model on the data like Logistic Regression,KNN,Random Forest,Naive Bayes,XGBoost with accuracy,pression,recall,F1-score and AUC as evaluation metrices.Among all the model XGBosst model performed very well with GridSearch CV as hyperparameter Tunning on both training and test data samples and this model was choosed as final model.

# EDA Conclusion
In our data set around 57% of the patients's gender was Female and around 49.8% of the patients are smokers.18.5% of the Male patients and 12.4% of Female patients and around 16.3% of the patients who are smokers and 13.8% of the non-smoker patients have chances of getting the disease
only 2.9% of the patient are taking BP medicines and only 0.6% of the patient has prevalent Stroke and around 31.5% of the patients has prevalent Hypertension and only 2.6 % of the patients has Diabetes and Only 15.1% of the patients has a chance of getting cardio-vascular disease in next 10 years
People at Education Level 1 have more chances of getting the disease than other Education Level
Majority of the patient's age were in the range of 40-50 and the chances of suffering with CHD increase with increase in age
Patients suffering with the prevalant stroke have more chances of suffering with the disease
Daibetes patients are having more glucose level and are more prone to CHD
Patients having Cholestrol greater than 300 mg/dl and less than 150 mg/dl are having more chances of getting the disease'
Patients having systolic Bp greater than 150 mmhg and less than 110 mmhg are having more chances of getting the disease
Patients having dia-Bp greater than 100 mmhg and less than 70 mmhg are having more chances of getting the disease
There is not a specific BMI which can lead to CHD but it can seen that patients with overweight and obese conditions i.e BMI >25 are have little more risk of getting CHD in future
Patients having heart rate more than 90 are having little more risk of getting the disease

# ML Conclusion
I have implemented Logistic Regression,Random forest,KNN,Naive Bayes and XGBoost model on my data. Based on the performance of all the models, i have selected XGBoost model as the final prediction model. The XGBoost model outperformed the other models in several key aspects, making it the preferred choice for prediction.

The XGboost model with hyperparamter tunning ,has performed very well with higher accuracy,recall,F1 score and AUC value of 99% on training and 94% on test.The best paramters was found to be 'gamma': 0.1, 'learning_rate': 0.1, 'max_depth': 7, 'n_estimators': 200. Out of 1152 patients our optimal model is correcly predicting 524 of class 0 and 499 of class 1 patients, other 100 and 23 are FN and FP cases. I have applied Feature importance method to find out what are the features that are important for the prediction of the target feature:

it can be seen that age feature is contributing the most around 21.7% followed by the BPMeds as 17.5 and then pulse_pressure around 13.12% and so on
