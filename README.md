# Yes-Bank-Stock-Closing-Price-Prediction

This repository contains the daaset of with the monthly stock prices of Yes Bank. There is are two notebooks, one that has been worked on individually by me, and another one which is a combined effort of the team. There is also a PDF of a presentation that summarizes our findings.

We have been provided with a dataset of the monthly stock price details of Yes Bank. The data has been provided from July 2005 till November 2020. The bank has been making headlines due to its recent default. We analysed the dataset and worked on predicting the stock closing price for the bank using other given parameters. 

To start with, we needed to understand each parameter of the dataset and the relationships between them. Hence, we performed Exploratory Data Analysis on the Data. Some skewness was observed in the parameters for which we performed the log transformation. Further analysis was performed on each variable with respect to each of the other variables. Moreover the same was visualised using the correlation matrix. We observed from the Correlation matrix the independent variables are highly correlated to all of the dependent variables. 

We performed Linear regression setting high, low and open as independent variables. Divided the dataset into training and testing datasets. We transformed the data using MinMax scaler which transforms each feature in a given range. We predicted the closing price of the test data using the Linear regression model we have trained.

Also, to check how other models perform, we performed Lasso regression and Ridge regression, both with alpha 0.1 and maximum iterations of 3000 with the same datasets used for training Linear regression. We performed Cross validation and got the best fit alpha value. We predicted the closing price of the test data using the Lasso regression model and ridge regression respectively. 

Moving forward, we calculated the various performance metrics like MAE, MAPE, MSE, RMSE, r2 scores for all the three models. Finally, we plotted the actual values vs predicted values of the closing price for all of them. Linear Regression has given the best results with lowest MAE, MSE, RMSE and MAPE scores. Ridge regression shrunk the parameters to reduce complexity and multicollinearity, but ended up affecting the evaluation metrics. Lasso regression did feature selection and ended up giving up worse results than ridge which again reflects the fact that each feature is important.

Although Linear Regression gives the best result of all three, the difference is very minute between all three. We use the Linear regression for our final prediction due to its simplicity. We used some other ensemble methods too, which gave almost the same results. We concluded this could be because all the independent variables are highly correlated with the dependent variable, the close price.

