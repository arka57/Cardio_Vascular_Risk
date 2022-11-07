# Cardio_Vascular_Risk
## **Cardio Vascular Disease Prediction**
The dataset is from an ongoing cardiovascular study on residents of the town of Framingham,
Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of
future coronary heart disease (CHD). The dataset provides the patients’ information. It includes
over 4,000 records and 15 attributes.


**Variables**<br />
Each attribute is a potential risk factor. There are both demographic, behavioral, and medical risk factors.


**Data Description**

**Demographic**:

• Sex: male or female("M" or "F")
• Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to
whole numbers, the concept of age is continuous)

**Behavioral**:

• is_smoking: whether or not the patient is a current smoker ("YES" or "NO")
• Cigs Per Day: the number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarettes, even half a cigarette.)

**Medical( history)**:

• BP Meds: whether or not the patient was on blood pressure medication (Nominal)
• Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)
• Prevalent Hyp: whether or not the patient was hypertensive (Nominal)
• Diabetes: whether or not the patient had diabetes (Nominal)

**Medical(current)**:

• Tot Chol: total cholesterol level (Continuous)
• Sys BP: systolic blood pressure (Continuous)
• Dia BP: diastolic blood pressure (Continuous)
• BMI: Body Mass Index (Continuous)
• Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though       in fact discrete, yet are considered continuous because of a large number of possible values.)
• Glucose: glucose level (Continuous)


**Predict variable (desired target)**
• 10-year risk of coronary heart disease CHD(binary: “1”, means “Yes”, “0” means “No”) -
DV



**Solution Approach**:

1)EDA and necessary feature engineering is done on the data to make it apt before feeding it to the ML models. Some features are either unrelated to the target varible or interrleated with other feature attributes

2)Classification task is performed using various approaches like Logistic Regression and tree based models-Decision Tree,Random Forest,GradientBoosting,XGBoost. Hyperparameter tuning is done on the above mentioned models using GridSearchCV

After applying the various approaches we observed the following results










## Metric:Accuracy<br>

|  Method                              | Train | Test  |
|--------------------------------------|-------|-------|
|Logistic Regression                   | 74.14 | 74.30 |
|Logistic Regression with GridSearchCV | 70.21 | 69.61 |                
|Decision Tree                         | 92.18 | 83.94 |
|Random Forest                         | 97.67 | 91.14 |
|Gradient Boosting                     | 100   | 91.57 |
|XGBoosting                            | 94.96 | 91.05 |

## Metric:Precision<br>

|  Method                              | Train | Test  |
|--------------------------------------|-------|-------|
|Logistic Regression                   | 66.72 | 69.09 |
|Logistic Regression with GridSearchCV | 75.52 | 77.09 |                
|Decision Tree                         | 92.18 | 83.94 |
|Random Forest                         | 97.67 | 91.14 |
|Gradient Boosting                     | 100   | 87.45 |
|XGBoosting                            | 90.21 | 84.72 |

## Metric:Recall<br>

|  Method                              | Train | Test  |
|--------------------------------------|-------|-------|
|Logistic Regression                   | 77.35 | 72.65 |
|Logistic Regression with GridSearchCV | 68.68 | 65.43 |                
|Decision Tree                         | 92.18 | 83.94 |
|Random Forest                         | 97.67 | 91.14 |
|Gradient Boosting                     | 100   | 91.57 |
|XGBoosting                            | 94.96 | 91.05 |


## Metric:ROC_AUC Score<br>

|  Method                              | Train  | Test   |
|--------------------------------------|--------|--------|
|Logistic Regression                   | 0.7375 | 0.7281 |
|Logistic Regression with GridSearchCV | 0.7040 | 0.7021 |                
|Decision Tree                         | 0.9218 | 0.8394 |
|Random Forest                         | 0.9773 | 0.9114 |
|Gradient Boosting                     | 1.00   | 0.9188 |
|XGBoosting                            | 0.9534 | 0.9174 |




