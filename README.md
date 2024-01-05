# Flight Fare Forecasting Web App

## Abstract - 
Optimal timing for airline ticket purchasing from the consumer’s perspective is challenging because consumers do not have enough information to justify future price changes. In this project, I’ve mainly targeted to uncover underlying trends of flight prices in India using a data set where I’ve been provided with prices of flight tickets for various airlines and between various cities—size of training set: 10683 records. Moreover, I’ll be hosting the API i.e. app in a web environment where the app will predict the price/fare of a single flight ticket based on the user inputs taken.

## Methodology -
Components of the working of this project can be divided into two main phases which will be discussed individually:
a)	Training the machine learning model
Training the dataset in the model is the project's major portion. Comprises of three sections:

i.	Handling categorical data-
Here, there are two types of categorical data to be dealt with mainly, Nominal data which are data not in any order (OneHotEncoder technique is used in this case) and Ordinal data which is in order (LabelEncoder is used in this case). OneHotEncoder is used when we need  to handle unordered data i.e there is no direct or indirect comparison between data entries in a column. This technique has been used for most of the pre-processing part.
LabelEncoder is used when we need  to handle ordered data where there is direct state of   comparison between data entries in a column and we need to assign values to them to rank them sequentially.

ii.	Feature Selection-
This process involves the search of the best feature out of the set of features considered important. The best feature will contribute the most and will have a direct relation with the target variable i.e price(in this case). Methods used for feature selection are creating heatmaps, finding positive and negative correlations between dependent and independent attributes and using feature_importance_ 

iii.	Hyperparameter tuning 
Hyperparameter optimization can be executed using one of the algorithms stated below:
1.	RandomizedSearchCV
2.	GridSearchCV
(CV = Cross Validation)

Under hyperparameter tuning we’ll be using Randomised Search CV which will do all sorts of permutation and combinations to find out that one value of the best parameter (found in the feature selection stage) which will give the highest accuracy in fare prediction/forecasting.

b)	Building the web app (.py) file 
We need to import Flask library for hosting the machine learning model attached with frontend in a web environment. For accepting inputs from user we use OneHotEncoding technique to convert string inputs into binary terms (0’s and 1’s).

## Website Images - 

![2020-12-27 (5)](https://github.com/SiddhantVerma09/flightfareforecastingweb/assets/63495865/b2d23643-7551-4f1f-9497-7ab25e2001af)

![2020-12-27 (4)](https://github.com/SiddhantVerma09/flightfareforecastingweb/assets/63495865/467ac8ee-5d32-4736-a9da-a83fa1dcf532)

