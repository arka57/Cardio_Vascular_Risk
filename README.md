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

After applying the various approaches we observed the following results. 
We analysed the effectiveness of the different models on various parameters like<br>
Accuracy( Not a very good measure for classification purpose)<br>
Precision<br>
Recall<br>
ROC-AUC Curve and Score<br>
Confusion Matrix<br>



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

### Confusion Matrix and AUC Curve<br>

![image](https://user-images.githubusercontent.com/36561428/200599224-67730efb-c8dd-486c-9d7a-326cffb9bc80.png)
![image](https://user-images.githubusercontent.com/36561428/200599343-efc27481-0566-4f74-a8dc-07cec6a5ae0f.png)
![image](https://user-images.githubusercontent.com/36561428/200599682-a50bb1a2-7913-46cc-994e-f0b469f27647.png)


## Logistic Regression with GridSearchCV


![image](https://user-images.githubusercontent.com/36561428/200599774-dbbe0bf4-1651-4b70-bb38-432f86682d47.png)
![image](https://user-images.githubusercontent.com/36561428/200599799-c907429f-1b97-4c72-8662-0c3c13e1daa0.png)
![image](https://user-images.githubusercontent.com/36561428/200599847-8e835f13-6559-4ade-be22-f4efd3361f71.png)
![image](https://user-images.githubusercontent.com/36561428/200599867-2377581f-f6cc-459e-81a5-4b337895dc94.png)

## Decision Tree

![image](https://user-images.githubusercontent.com/36561428/200599984-452f25fb-6d1d-473c-81fb-c0b9f415fa34.png)
![image](https://user-images.githubusercontent.com/36561428/200600032-840e33ac-a00c-4d33-929a-7320dd92b2e9.png)
![image](https://user-images.githubusercontent.com/36561428/200600064-a65e8258-8e57-4419-89c0-ac43c8108994.png)
![image](https://user-images.githubusercontent.com/36561428/200600090-22a3aff3-82b7-47a8-922a-a2df73d40f7c.png)

## Random Forest

![image](https://user-images.githubusercontent.com/36561428/200601630-710ba256-4905-4aff-b83d-2ec239c647e2.png)
![image](https://user-images.githubusercontent.com/36561428/200601660-c76d6da9-4e52-40d0-a2cb-8f9409f094d4.png)
![image](https://user-images.githubusercontent.com/36561428/200601690-249d8521-aa70-47b4-bc25-2231ad97e5d1.png)
![image](https://user-images.githubusercontent.com/36561428/200601709-7d307064-844e-4c27-b7fd-3fb77282c7ef.png)

## Gradient Boosting

![image](https://user-images.githubusercontent.com/36561428/200601802-295b9a53-6728-405e-a565-912b38b874de.png)
![image](https://user-images.githubusercontent.com/36561428/200601846-271abbbc-e0e8-4465-89e0-d33d4ea17f9b.png)
![image](https://user-images.githubusercontent.com/36561428/200601880-4c9f9867-2703-4486-a121-f48c935a7ee4.png)
![image](https://user-images.githubusercontent.com/36561428/200601936-af0252de-83ae-47af-87d5-ed5fac81bb3b.png)

## XG Boosting

## Conclusion
1) There was significant improvement in model performance as we moved from Logistic Regression to tree based models
2) We observed a bit of overfitting in the models showing a difference in training and testing data scores
3) Comparing all parameters XGBoost gave the best performance

