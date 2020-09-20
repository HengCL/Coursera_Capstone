# Coursera_Capstone_Report
HengCL Applied Data Science Capstone

## Introduction/ Business Problem
Seattle Police Department had been recording all types of vehicular collisions that often times lead to a loss of property and the lives of those involved. The question that can be raised here is as such-"What are the most common causes, in order to prevent road accidents from happening?". This is an attempt to understand the factors and their correlations based on data collected from 2004 to the present. With the results of the analysis, preventive measures could be introduced to the SPD for better enforcement strategies of safety protocols or maybe, to help provide better advise for drivers during critical weather conditions through existing communication technology like apps.

## Data
The dataset used for this project is based on car accidents which have taken place within the city of Seattle from the year 2004 to 2020. This data is regarding the severity of each car accidents along with the time and conditions under which each accident occurred. The chosen model aims to predict the severity of an accident, considering that, the variable of Severity Code was in the form of 1 (Property Damage Only) and 2 (Physical Injury) which were encoded to the form of 0 (Property Damage Only) and 1 (Physical Injury). Following that, 0 was assigned to the element of each variable which can be the least probable cause of severe accident whereas a high number represented adverse condition which can lead to a higher accident severity. Whereas, there were unique values for every variable which were either Other or Unknown, deleting those rows entirely would have led to a lot of loss of data which is not preferred.

In order to deal with the issue of columns having a variation in frequency, arrays were made for each column which were encoded according to the original column and had equal proportion of elements as the original column. Then the arrays were imposed on the original columns in the positions which had Other and Unknown in them. This entire process of cleaning data led to a loss of almost 5000 rows which had redundant data, whereas other rows with unknown values were filled earlier.

![Image1](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/Frequency%20in%20data%20entry%20for%20each%20variable.png)

In order to deal with the issue of columns having a variation in frequency, arrays were made for each column which were encoded according to the original column and had equal proportion of elements as the original column. Then the arrays were imposed on the original columns in the positions which had Other and Unknown in them. This entire process of cleaning data led to a loss of almost 5000 rows which had redundant data, whereas other rows with unknown values were filled earlier.

At the end, the variables that were included in this analysis are the following:
1) INATTENTIONIND - Was the driver inattentive? (Y/N)
2) UNDERINFL - Was the driver under the influence? (Y/N)
3) WEATHER - Weather condition during time of collision? (Overcast/Rain/Clear)
4) ROADCOND - What was the road condition during collision? (Wet/Dry)
5) LIGHTCOND - What were light conditions during collision? (Lights On/ Dark with Light On)
6) SPEEDING - Was the car over the speed limit? (Y/N)

## Methodology

### Exploratory Data Analysis
Considering that the feature set and the target variable are categorical variables with the likes of weather, road condition and light condition being an above level 2 categorical variables whose values are limited and usually based on a particular finite group whose correlation might depict a different image then what it actually is. Generally, considering the effect of these variables in car accidents are important hence these variables were selected. A few pictorial depictions of the dataset were made in order to better understand the data.

![Image2](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/Accident%20locations%20at%20Seattle.png)

From the image above, the data had been cleaned to indicated the most common locations that accidens occured in Seattle. This gives us some better understanding on the situation on the ground where we can distribute the data onto the map of Seattle itself. This will help us in developing a resource distribution plan later. 

![Image3](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/No.of%20reported%20accidents%20located%20on%20Seattle%20map.png)

The factor which had most number of accidents under adverse conditions was adverse weather conditions while adverse lighting condition had the second most number of accidents caused by it. The factors which contributed the least to an instance of an accident are over-speeding and the driver being under the influence.

### Machine Learning Models Selected
1) Logistic Regression- Logistic regression is a statistical model that in its basic form uses a logistic function to model a binary dependent variable
2) Decision Tree Analysis: The Decision Tree Analysis breaks down a data set into smaller subsets while at the same time an associated decision tree is incrementally developed. The final result is a tree with decision nodes and leaf nodes.

## Results

### Decision Tree Classifier
![Image4](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/Decision%20Tree%20Accuracy.png)

Decision Tree Confusion Matrix:
![Image5](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/Decision%20Tree%20Matrix.png)

### Logistic Regression
![Image6](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/Logistic%20Regression%20Accuracy.png)

Logistic Regression Matrix:
![Image7](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/Logistic%20Regression%20Matrix.png)

## Model Accuracy

1) Precision: Precision refers to the percentage of results which are relevant, in simpler terms it can be seen as how many of the selected items from the model are relevant. Mathematically, it is calculated by dividing true positives by true positive and false positive
2) Recall: Recall refers to the percentage of total relevant results correctly classified by the algorithm. In simpler terms, it tells how many relevant items were selected. It is calculated by dividing true positives by true positive and false negative
3) F1-Score: f1-score is a measure of accuracy of the model, which is the harmonic mean of the model’s precision and recall. Perfect precision and recall is shown by the f1-score as 1, which is the highest value for the f1-score, whereas the lowest possible value is 0 which means that either precision or recall is 0

![Image8](https://github.com/HengCL/Coursera_Capstone/blob/master/Images/Summary.png)

## Conclusion
When comparing all the models by their f1-scores, Precision and Recall, we can have a clearer picture in terms of the accuracy of the three models individually as a whole and how well they perform for each output of the target variable. When comparing these scores, we can see that the f1-score is highest for Logistic Regression at 0.6. When looking at the other two models, we can see that the Decision Tree has a more balanced precision for 0 and 1 in terms a variance. Whereas, the Logistic Regression is more balanced when it comes to recall of 0 and 1. Furthermore, the average f1-score of the two models are very close but for the Logistic Regression it is higher by 0.04. It can be concluded that the both the models can be used side by side for the best performance. 

However, in this particular case we will select Logistic Regression due to its higher f1-score. 

## Recommendations
After assessing the data and the output of the Machine Learning models, a few recommendations can be made for the stakeholders. By using the Logistic Regression model and referring to the map created in the image above, SPD will be able to predict which areas have a higher chances of causing injury related accidents. Resources will be scarce and it would be wise for the SPD to focus on regions with the highest accidents. A priority and risk management plan could be executed to fix the lights or provide better road conditions. 

Besides that, special activated apps on a vehicles dashboard can be used to warn a driver whether the location that they are heading have what quantitative value of an accident happening. The future introduction of AI in vehicles to help accident prevention could play a very important role with the data we have now. 
