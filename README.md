# Project 2: Predicting Sale Price of Homes in Ames, Iowa
 ## Problem Statement
 What is the best price to list a house in Ames, Iowa? As a real estate broker, it is important to know what price a client should list their home in order to obtain the most value and  for it to sell in a reasonable time. Our goal is to build a model using data from 2006-2010 to predict a baseline sale price for homes in Ames, Iowa that also provides manners in which the seller can increase the home’s value.

## Executive Summary

The goal of this project is to accurately predict the sale price of a home in Ames, Iowa by utilizing data cleaning, EDA, preprocessing and linear regression models. The datasets used were provided by Kaggle and contained a comprehensive list of over 2,500 homes sold in Ames, Iowa between 2006 and 2010. The datasets also included 79 different features of a home. This data provided the framework for our data analysis to find the features that could best predict sale price. 

Before building our model, we needed to understand the dataset in greater detail. In order to do this, we first cleaned the data to make sure there were no missing values and that all data types for each feature were correct. We turned the nominal categorical features into dummy variables and created a scale for the ordinal features.   

After cleaning the data, we wanted to understand the relationship between the features and sale price by looking for possible trends as well as collinearity. We examined histograms and scatter plots for the numerical features and looked at bar charts for the categorical features. It became clear when seeing the graphs that many of the numerical features distributions were skewed to the right and had a positive relationship with sale price, especially the features related to square footage. This makes sense. The larger the house, the higher the selling price. We noticed that several of the categorical features also had a positive relationship with sale price. For example, as the overall quality of a house increased, so did the sale price. 

After scaling the data and selecting features to include in our analysis, I began to build several linear regression models to predict the sale price of a home. The best model would have the lowest root mean squared error for the training and test data. The three models built utilized Linear, LASSO and Ridge regression. 

 
 ## Data Dictionary
 - [Original Features](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt) 
 
 - New Features
 ---
|Feature|Type|Dataset|Description|
|---|---|---|---|
|Inside_SF|float|Training/Test|Sum of square footage inside a home|
|Bsmt Qual * Bsmt Cond|float|Training/Test|Interaction term between basement quality and condition|
|Fireplaces * Fireplace Qu|float|Training/Test|Interaction term between fireplaces and fireplace quality|
|Gareage Area * Garage Cond|float|Training/Test|Interaction term between garage area and condition|

## Conclusions and Recommendations
After cleaning, perfoming EDA, preprocessing and modeling the data, we were able to build a model that could capture over 90% of the variability in sales price for homes sold in Ames, Iowa between 2006-2010. Our root mean squared error for the Kaggle test data was approximately $20,000.

The model we used was a LASSO regression model. This model had the best root mean squared error and was not as overfit as the Ridge and Linear regression models. The features that predicted sales price the best were related to square footage and quality/condition of the home.

A real estate broker or potential home seller can use this model to accurately predict a baseline listing price for his/her home so they can get the most value and so it sells in a reasonable amount of time. The model can also be used to increase the value of a home. A homeowner can focus on improving some of the features that are highly positively correlated with sales price and removing features that are negatively correlated.

An area of concern in our model is the collinearity of features that are being utilized. Ideally, all the features within a model will be independent, but this is unrealistic. Another concern are the categories for the ordinal variables. We are unsure how the scales were created or chosen for each home. We would also like to have seen data more recent than 2010. The dataset examined could have been from the 2008 recession which took a big toll on real estate prices.

Overall, the model we created is very useful for prediciting home prices in Ames, Iowa. Other cities in the US would require additional data and analysis.



## Resources
- [https://www.kaggle.com/c/dsi-us-8-project-2-regression-challenge/data](https://www.kaggle.com/c/dsi-us-8-project-2-regression-challenge/data)
- [https://en.wikipedia.org/wiki/Ames,_Iowa](https://en.wikipedia.org/wiki/Ames,_Iowa)
- [https://plasticinehouse.com/roof-styles-sheds/](https://plasticinehouse.com/roof-styles-sheds/)
- [https://www.trulia.com/real_estate/Ames-Iowa/](https://www.trulia.com/real_estate/Ames-Iowa/)

