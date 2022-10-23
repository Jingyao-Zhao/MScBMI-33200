# Machine-Learning-Approaches-in-Breast-Cancer-Survival-Prediction

The dataset we are going to focus on to analyze and predict is the Real Breast Cancer Data, 
which consists of a group of breast cancer patients after taking the surgery to remove the tumor. 
Machine learning models are used in the process of breast cancer survivability of patient status.

# Dataset Details

The dataset consist 9351 rows with 16 columns including gender, age, protein type, tumour_stage, and patients_status etc.
We cleaned the dataset by dropped the rows with NA and excluded the irrelevant features such as patients id and patients visit, etc. 
Before putting data into models, Exploratory Data Analysis (EDA) process will be used to help us maximize the insights of the dataset and prepare to make the data cleaner and easier to be trained. We found major age range of breast cancer patients is from 45yrs to 65yrs from numerical distribution plot.

Also, we proved for each of numerical feature which is independent with the other by applying pearson correlation. 

<img src="https://user-images.githubusercontent.com/114511149/197402979-70999dd9-f1e8-4eed-a924-a2cf4cca7d7e.png" width=50% height=50%>

# Machine learning 

First we encoded categorical data values by using LabelEncoder to labelize the categorical data. It is used to convert categorical data into numbers.
Then we split the data into training and test data set. 
Feature scaling was applied to bring all features to the same level of magnitudes, because dataset contains features highly varying in magnitudes.
We transformed data so it fits specific scale, like 0-100 or 0-1.

Here are metrics for different machine learning models: 

Logistic regression: 
Accuracy: 0.796875 AUC:0.5

Logistic regression(with regularization):
Accuracy: 0.796875 AUC: 0.52

KNN: 
Accuracy: 0.75 AUC:0.49

SVM:
Accuracy: 0.79 AUC:0.5

Decision Tree:
Accuracy: 0.78 AUC:0.63

By comparing the error metrics of models and due to the  skewed characteristic of the dataset, instead of focusing on accuracy, 
I depend on four other metrics to figure the best performed model which is decision trees and it has 0.63 AUC, 0.85 precision, 0.88 recall and 0.87 F1 score.

And we found all four protein type and age are top five important features. 
<img src="https://user-images.githubusercontent.com/114511149/197403284-8bef72bf-981e-4742-8adf-423ed92d0cc5.png" width=50% height=50%>
