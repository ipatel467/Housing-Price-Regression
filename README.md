# Housing Price Regression
#### By: Ibrahim Patel

## Executive Summary
I wanted to make a regresion model that can predict the price of a house based on ceratin features. I gathered my Data from a Kaggle dataset, which is free for anyone to access. According to my finding I have found that there are some features that people should take into consideration when purchasing a home.

## Contents
1. [Introduction](#introduction)
    - [Problem Statement](#problem_statement)
    - [Dataset](#dataset)
2. [Analysis](#analysis)
    - [Data Cleaning](#data_cleaning)
    - [Exploratory Analysis](#exploratory_analysis)
    - [Modeling](#modeling)

## Introduction <a name="introduction"></a>
I am really interested in real estate, so I thought this would be a fun project. I am going to go through what features have an effect on the price of the house. I will be using an OLS model for this project.

### Problem Statement <a name="problem_statement"></a>
I want to make a Linear Regression model that can predict my Target varaible(Price) as accurately as possible. The way this can be figured out is by Feature Selection. After we have our selected features we will run an OLS. These features variables will help me predict my target(Price).

### Dataset <a name="dataset"></a>

https://www.kaggle.com/lodhaad/house-prices

## Analysis <a name="analysis"></a>
After cleaning and dropping many features I did a train test split to split my data into training and test categories. Then I ran an OLS and got an R Squared of .44. An R squared of .44 is not bad, however, I would like to make it better. My model is under fit due to the lack of features. However, there is a simple fix to an underfit model. I started again from the begining and dropped less features than before. After adding more feautres to my model I ran an OLS I got an R Squared of .595. My model improved my roughly 15% by adding 4 extra features.

### Data Cleaning <a name="data_cleaning"></a>
This dataset was very messy, and very clean at the same time. I had a lot of values that were placed in as 0's instead of NaN. That made dropping things a little more tricky. Some of the features where not normally distibuted so I had to normalize them. I also had to deal with a good amount of outliers. I did not want the outliers to mess up my model, so I Used SciPy Z- scores. I removed anything that had an absolute value Z-score over 2.5. I ended up removing roughly 3000 outliers.

 

### Exploratory Analysis <a name="exploratory_analysis"></a>

I found that the 3 top features in my dataset are view, bathrooms, and sqft_living. These 3 features have the highest Coefficents, and they are all significant. I used 6 Features for my model the first time around which captured 44% of my data. Then I added 5 more features into my model. I ran the model a second time with 11 features and it raised my R-Squared to .595, which is good because this new model captures 59.5% of the data.



### Modeling <a name="modeling"></a>
I used Lasso Regression first to see which are the most important features. After doing that I used an OLS stats model to run my Regression model. My final model gave me an R-Squared of appx .60. So this shows that my model captures 60% of my data, which is an improvement from my first model. To improve my model I would need to implement some new features so my model can have a better fit and accuracy. 


