# :stethoscope: Project_4 - Machine Learning Integration - Heart Disease :stethoscope:

![MainImage_A1-9](https://user-images.githubusercontent.com/115706722/231760675-8931fa50-9867-49f4-a601-3afe90e3e1e0.jpg)

## Contents

* [Project Overview](#project-header)
* [Dataset](#dataset-header)
* [Tools used](#tools-header)
* [the Process](#process-header)
* [Report](#reports-header)
* [Presentation](#presentation-header)
* [Team](#team-header)

## <a id="project-header"></a>Project Overview 

This project analyses heart disease using machine learning (ML) models and predicts the likelihood that patients will suffer from heart disease based on relevant contributing features from the dataset. We use a SQL relational DB and make use of binary classification models such as `logistic regression` and `decision trees`. We visualised this problem and our analysis, the results for which may be seen in the [Report](#reports-header).


## <a id="dataset-header"></a>Dataset 

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



 ## <a id="process-header"></a> Process
 
Preprocessing and cleaning the data was the first step in creating our ML models

- We checked for null and duplicate values in the dataset
- Then we used `get_dummies` to convert categorical values with misleading values (Eg Thallium categories '3', '6', '7' to dummie values in the data, which may be fed to the algorithm and yield accurate results and scores.
<img width="1013" alt="Screenshot 2023-04-18 at 11 21 59" src="https://user-images.githubusercontent.com/115706722/232748839-ab8268d0-0c54-4b58-a73c-d9f8d73f53b3.png">
- Finally we updated the DataFrame with the dummie, made a copy and then dropped the Heart Disease Column ready to be split into train and test groups and 
 <img width="1015" alt="Screenshot 2023-04-17 at 10 56 48" src="https://user-images.githubusercontent.com/115706722/232750114-3864749a-99f3-474c-aede-d99816ef24ca.png">
- We then scaled the rest of the data so it could be accurately fit to the model
 

<img width="730" alt="Screenshot 2023-04-17 at 11 13 07" src="https://github.com/gussiepoole/Heart-Disease-Project/assets/115706722/1b6d535b-fa8d-4941-a7cd-a74fb9fee981">

## **<a id="reports-header"></a>:trophy: What we were able to achieve: :trophy:**
* Although we trialled a lot of different methods and optimizations inluding Hyperparameters Tuning the most successful model we created was with Logistic Regression.
* We optimized 3 versions of this model and were able to achieve an **overall score of 88.24%** 


:2nd_place_medal: **1st Attempt - Logistic Regression Model**
Target values:

0: 150

1: 120

Outcome:
Overall Accuracy: 88.24%

Recall - the model predicts '0' (healthy) as 89% and '1' (with heart disease) as 87%.

<img width="982" alt="Screenshot 2023-05-30 at 10 37 32" src="https://github.com/gussiepoole/Heart-Disease-Project/assets/115706722/e97f16c8-0003-48e6-a605-d4bcc1f59d51">


🥉 **2nd Attempt - Logistic Regression Model with Resampled Training Data** 
Target values:

0: 112

1: 112

Outcome:
Overall Accuracy: 86.76%

Recall - the model predicts '0' (healthy) as 89% and '1' (with heart disease) as 84%.


:1st_place_medal:	**3rd Attempt - Logistic Regression Model with Hyper Parameters Tuning (GridSearchCV)**

penalty:l2

solver: lbfgs, newton-cg, saga

Outcome:
Best Score: 82.75
Overall: 88.24%



**Why We Chose This Model**

* We chose this the Logistic Regression Model because it is proven to be effective for binary classification, which several of our group had experienced success with when working on a similar kind of casetsudy in the past.

* This kind of model also aligned with the context of our project. In logistic regression, the model learns a relationship between the input features and the probability of the output being one of the two classes. 

* The clear aims of our model in predicting a presence or absence of Heart Disease is displayed in the output of a logistic regression model by a probability score between 0 and 1. 



 ## :wrench: <a id="tools-header"></a> Built With :wrench:
 
 - `Python Pandas`, `Matplotlib`
 - `SQL Database`
 - `Neural Networks`, `Logistic Regression`, `Decision Tree`, `GridSearchCV`
 - `Sklearn.metrics`
 - `Tensorflow`
 - `Tableau`

 ## <a id="presentation-header"></a>Presentation


[Link to our presentation created on Tableau](https://public.tableau.com/app/profile/marta8505/viz/HeartDiseasePrediction_16816724810860/Homepage?publish=yes)

<img width="1098" alt="Screenshot 2023-05-30 at 10 47 24" src="https://github.com/gussiepoole/Heart-Disease-Project/assets/115706722/badaeec4-cad8-42a6-ae1e-351128b789b2">

 
## <a id="team-header"></a>Team
* [Tony](https://github.com/TonyHHNg)
* [Maria](https://github.com/MariamaDoumb)
* [Marta](https://github.com/rychema)
* [Gussie](https://github.com/gussiepoole)

