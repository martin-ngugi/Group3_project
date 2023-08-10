# Group3_project

![Alt text](image.png)
## Analyzing the impact  of weather conditions and ride demands  on Uber and lyft rides in relation to price.
### 1. Business understanding
### a) Introduction

Ride-sharing services Uber and Lyft, have transformed the way people commute and travel in urban environments. These companies have disrupted the olden ways of the taxi industry by harnessing the power of technology to create a seamless and convenient transportation experience for riders. The ride-sharing services that is coming up at a high rate has led to a shift in urban mobility, giving people another easier way of transportation. 
The Uber and Lyft is found via a mobile application that connects riders with nearby drivers, enabling users to request rides with just a few taps on their smartphones. This user-friendly and efficient model has gained immense popularity country and worldwide, making ride-sharing a ubiquitous part of modern urban living. The applications receive millions of rides being requested and completed every day.  
Understanding the impact of external factors, such as weather conditions, on ride demand and pricing is of paramount importance for these transportation companies. Weather conditions can significantly influence ride patterns, rider preferences, and even the availability of drivers. For instance, heavy rainfall may increase demand for rides, leading to higher surge pricing and longer waiting times. During pleasant weather, riders may be more inclined to opt for shared rides or longer-distance options hence causing many people to cancel their rides.
The goal of this data science project is to dive into the relationship between weather conditions and ride services to see what relationships and trends that can enhance operational efficiency and customer experience. 

### b) Problem statement
The goal of this project is to explore the relationship between weather conditions and the ride services that have been provided by Uber and Lyft. Therefore building a model to analyze the impact of weather conditions, time and availability of the ride on the pricing. Our goal is to develop classification models that uses data on past Uber and Lyft services to accurately capture the relationship between weather condition and ride hailing services and their impact on cab prices.

### d) Main Objective
To understand how weather conditions affect the demand for cabs and how this, in turn, affects the price of cab rides.

##### i) Specific objectives
* Identify  factors that affect  demand for cabs in different weather conditions
* Develop models that can predict the demand for cabs and the price of cab rides at different times and weather conditions.
* Describe how the time of the day affects the cab prices.
* Determine what cab is preferred by the clients
* Discuss how the distance affects the pricing of the cab.
### f) Data Understanding
This analysis will use data from Kaggle, Uber and Lyft dataset. The dataset has 693,071rows and 10 columns. The dataset includes information such as cab type, destination, source and price. There is also a weather dataset based on weather conditions and how they affect the pricing of the cabs. It has 6,276rows and 18columns. The dataset contains information like temperature, location, clouds, pressure and rain.

### Modeling
#### First Model: Linear Regression
Dep. Variable: This indicates the dependent variable in your model, which is "price" in this case.

R-squared is the coefficient of determination, a measure of how well the independent variables explains the variability the dependent variable. An R-squared value of 0.927 means that approximately 92.7% of the variability in the dependent variable (price) is explained by the independent variables in our model.
Mean squared Error (MSE) is the average of the squared differences between the predicted values and the actual values.A lower MSE indicates that the model's predictions are closer to actual values.In this case, the MSE is approximately 6.32, which means that, on average, the squared difference between the predicted prices and the actual prices is around 6.32.

Root Mean Squared Error(RMSE) is the square root of the MSE. The RMSE gives you an idea of the typical magnitude of the errors in the predictions.Like the MSE, a lower RMSE indicates better performance. In this cae, the RMSE is approximately 2.51, meaning that the typical difference between the predicted prices and the predicted prices and the actual prices is around 2.521 units.

In summary, both the MSE and RMSE provide insights into how well your regression models predictions align with the actual values. Lower values indicate better predictive performance, as they signify smaller prediction errors.
#### Second model: Multi linear regression
The following were the findings after modeling;
The intercept is the value of the dependent variable when all of the independent variables are 0. In this case, the intercept is -8.91.

The mean squared error is a measure of how well the model fits the data. In this case, the mean squared error is 6.28.

The R-squared score is a measure of how much of the variation in the dependent variable is explained by the independent variables. In this case, the R-squared score is 0.92, which means that 92% of the variation in the dependent variable is explained by the independent variables.

The root mean squared error is the square root of the mean squared error. In this case, the root mean squared error is 2.5.

Overall, this model seems to fit the data well, as evidenced by the high R-squared score and low mean squared error.
#### Third model: Ridge Regression
The following were the findings after modeling and evaluation;
MSE of 6.29 means that, on average, the squared difference between predicted and actual values is 6.29. Lower values are better. An R-squared of 0.93 means that the model explains about 93% of the variance in the target variable. An MAE of 1.78 means that, on average, the absolute difference between predicted and actual values is 1.78.
The Ridge model with the best alpha value of 0.00001 achieved a good level of performance on the test data. It provides relatively low Mean Squared Error, high R-squared (indicating good explanatory power), and low Mean Absolute Error, which collectively suggest that the model is making accurate predictions and generalizing well to unseen data. This outcome implies that the chosen Ridge model with the best hyperparameter configuration is a suitable choice for predicting cab prices based on the provided features.

#### Fourth model: Decision Tree Regression.
The target variable used for regression model was price.

Hyperparameter tuning using gridsearch cross validation. The best parameters were found to be:
* max_depth = 5
* min_samples_leaf =1
* min_samples_split = 2

After using these parameters, the model was evaluated using mean squared error, root mean squared error and the rsquared

After modelling the results were, an MSE of 17.04, which suggests that the models predictions deviate from the actual values by an average squared difference of 17.04 units. R-squared of 0.8 indicates that approximately 80% of the variance in the target variable is explained by the model. This means the model captures a substantial portion of the relationship between the input features and the target variable.

#### Fifth Model: Logistic Regression
After modelling, these were the results after evaluating the model.
A cross validation score of 0.88 which indicates that the logistic regression model is doing a good job of predicting the outcome. The closer the cross validation score is to 1, the better the model is at predicting the outcome.

#### Sixth Model: Random Forest
The mean absolute error (MAE) is a measure of how close the model's predictions are to the actual values. In this case, the MAE is 0.09, which means that the model's predictions are on average 0.09 units away from the actual values.

The mean squared error (MSE) is a measure of how much the model's predictions vary from the actual values. In this case, the MSE is 0.04, which means that the model's predictions vary on average 0.04 units from the actual values.

The root mean squared error (RMSE) is the square root of the MSE. In this case, the RMSE is 0.21, which means that the model's predictions vary on average 0.21 units from the actual values.

The R-squared score is a measure of how well the model fits the data. In this case, the R-squared score is 0.82, which means that the model explains 82% of the variation in the data.

Overall, these metrics indicate that the Random Forest regression model is doing a good job of predicting the data.

### Conclusion
1. The best performing model was selected based on the mse and rmse values which makes the random forest model be the best performing mmodel. 

    * Random Forest - Mean Absolute Error: 0.09040000000000001
    
    * Random Forest - Mean Squared Error: 0.044871999999999995

2. When the temperature gets higher from a degree of 35 to 50 there is an increase in cab prices caused by higher demand

3. When there is low rainfall the prices are  higher due to high demand compared to when there is high rainfall.

4. Uber is preferred to Lyft

5. An increase in distance contributes to an increase in price in  the different cab types

### Recommendation
1. Lyft should do more marketing so that more people are aware of it and order more of the cabs.

2. Both Uber and Lyft should continue using their dynamic pricing strategies(surge pricing), based on factors like weather conditions, demand-supply ratios, and time of day.

3. Creating loyalty programs to attract and maintain customers.

4. Customizing a customer's travel experience.