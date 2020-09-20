# Coursera_Capstone
HengCL Applied Data Science Capstone

## Introduction/ Business Problem
Seattle Police Department had been recording all types of vehicular collisions that often times lead to a loss of property and the lives of those involved. The question that can be raised here is as such-"What are the most common causes, in order to prevent road accidents from happening?". This is an attempt to understand the factors and their correlations based on data collected from 2004 to the present. With the results of the analysis, preventive measures could be introduced to the SPD for better enforcement strategies of safety protocols or maybe, to help provide better advise for drivers during critical weather conditions through existing communication technology like apps.

## Data
The dataset used for this project is based on car accidents which have taken place within the city of Seattle from the year 2004 to 2020. This data is regarding the severity of each car accidents along with the time and conditions under which each accident occurred. The chosen model aims to predict the severity of an accident, considering that, the variable of Severity Code was in the form of 1 (Property Damage Only) and 2 (Physical Injury) which were encoded to the form of 0 (Property Damage Only) and 1 (Physical Injury). Following that, 0 was assigned to the element of each variable which can be the least probable cause of severe accident whereas a high number represented adverse condition which can lead to a higher accident severity. Whereas, there were unique values for every variable which were either Other or Unknown, deleting those rows entirely would have led to a lot of loss of data which is not preferred.

