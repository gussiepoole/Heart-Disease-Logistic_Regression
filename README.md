# Project_4 - Machine Learning Integration - Heart Disease

![MainImage_A1-9](https://user-images.githubusercontent.com/115706722/231760675-8931fa50-9867-49f4-a601-3afe90e3e1e0.jpg)

## Contents

* [Dataset](#dataset-header)
* [Project Outline](#project-header)
* [Tools used](#tools-header)
* [Inight into the Process](#process-header)
* [Report](#reports-header)
* [Presentation](#presentation-header)
* [Challenges](#challenge-header)
* [Team](#team-header)



## :stethoscope: <a id="dataset-header"></a>Dataset :stethoscope:

Our Dataset was a CSV file with 270 records, sourced from Kaggle[https://www.kaggle.com/datasets/rishidamarla/heart-disease-prediction] 


**Understanding the Dataset** 

* Chest pain type - Typical angina, Atypical angina, Non-anginal pain, Asymptomatic 
* BP (Blood Pressure)
* Cholesterol
* FBS over 120
* EKG results
* Max HR
* Exercise angina
* ST depression
* Slope of ST (The slope of the peak exercise ST segment) - Upsloping, Flat, Downsloping 
* Number of vessels fluro (Number of major vessels (0-3) colored by flourosopy)
* Thallium - Normal, Fixed defect, Reversable defect 
* Heart Disease - Absence or Presence

## :memo: <a id="project-header"></a>Project Outline :memo:

This project analyses heart disease using machine learning (ML) models and predicts which patients are most likley to suffer heart disease based on features that result in heart disease. We visualised this problem and our analysis, the report for which may be seen in the Report section(#reports-header)
We used binary classification models that predict the absence or presence of Heart Disease.

 ## :wrench: <a id="tools-header"></a>Tools used :wrench:
 
 - `Python Pandas`, `Matplotlib`
 - `SQL Database`
 - `Neural Networks`, `Logistic Regression`, `Decision Tree`, `GridSearchCV`
 - `Sklearn.metrics`
 - `Tensorflow`
 - `Tableau`

:trophy: We were able to achieve: :trophy:
* Although we trialled a lot of different methods and optimizations inluding Hyperparameters Tuning the most successful model we created was with Logistic Regression.
* We optimized 3 versions of this model and were able to achieve an overall score of  88.24% 

1st Attempt - Logistic Regression Model
Target values:
0: 150
1: 120
Outcome:
Overall Accuracy: 88.24%
Recall - the model predicts '0' (healthy) as 89% and '1' (with heart disease) as 87%.

2nd Attempt - Logistic Regression Model with Resampled Training Data
Target values:
0: 112
1: 112
Outcome:
Overall Accuracy: 86.76%
Recall - the model predicts '0' (healthy) as 89% and '1' (with heart disease) as 84%.

:1st_place_medal:	3rd Attempt - Logistic Regression Model with Hyper Parameters Tuning (GridSearchCV)
penalty:l2
solver: lbfgs, newton-cg, saga
Outcome:
Best Score: 82.75
Overall: 88.24%





**Why We Chose This Model**
We chose this the Linear Regression Model because it is proven to be effective for binary classification, which several of our group had experienced success with when working on a similar kind of casetsudy in the past.

This kind of model also aligned with the context of our project. In logistic regression, the model learns a relationship between the input features and the probability of the output being one of the two classes. 

The clear aims of our model in predicting a presence or absence of Heart Disease is displayed in the output of a logistic regression model by a probability score between 0 and 1. 

 ## <a id="process-header"></a>Insight into the Process
 
 Our first steps in creating our ML models was to complete preprocessing and clean the data.

- We checked for null and duplicate values in the dataset
- Then we used `get_dummies` to convert categorical values with misleading values (Eg Thallium categories '3', '6', '7' to dummie values in the data, which may be fed to the algorithm and yield accurate results and scores.
<img width="1013" alt="Screenshot 2023-04-18 at 11 21 59" src="https://user-images.githubusercontent.com/115706722/232748839-ab8268d0-0c54-4b58-a73c-d9f8d73f53b3.png">
- Finally we updated the DataFrame with the dummie, made a copy and then dropped the Heart Disease Column ready to be split into train and test groups and 
 <img width="1015" alt="Screenshot 2023-04-17 at 10 56 48" src="https://user-images.githubusercontent.com/115706722/232750114-3864749a-99f3-474c-aede-d99816ef24ca.png">
 

 ## <a id="presentation-header"></a>Presentation


 Link to our presentation created on Tableau [******]
 
We Logistic regression is a type of statistical model used for binary classification, which means that it predicts one of two possible outcomes. In logistic regression, the model learns a relationship between the input features and the probability of the output being one of the two classes. The output of a logistic regression model is a probability score between 0 and 1, which represents the likelihood of the instance belonging to the positive class which suits the structure of our data set is predicting the patient is likely to have heart disease or not.
 
## <a id="team-header"></a>Team
* [Tony](https://github.com/TonyHHNg)
* [Maria](https://github.com/MariamaDoumb)
* [Marta](https://github.com/rychema)
* [Gussie](https://github.com/gussiepoole)

