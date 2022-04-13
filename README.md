# Datathon_Amazon
Participation in the Amazon Datathon Newset: https://www.kaggle.com/c/newset-datathon-2022
Final ranking on Kaggle not correct due to a bug in submission. Our Team 'DataTuna' ranked place 12/28 with an RMSE of 275 (best team 152)

## Backlog Prediction: MNR/Earlies Expected
Inside AMZL Operations exists EU CO Forecast, a team that owns EU short term planning Out for Delivery (OFD) volume forecast. In a few words, the team predicts how many packages will arrive at Delivery Stations, so operation capacity can be adjusted accordingly. To properly deliver the task, the team needs to understand customer behaviour, upstream network connections and capacity, delivery stations capacity and available on the road capacity.

One of the most important processes for the team, apart from predicting incoming packages, is to properly protect customers by setting up CAPs based on downstream capacity. To ensure high performance on both processes, it is important to break them down into pieces that allow a better understanding and predictability.

## Goal
Design a regression algorithm to predict the difference between Earlies_Expand MNR_Exp based on a training dataset holding 5 months of historical values (01/02/2021 - 30/06/2021). The aim will be to create a feasible forecast for EU Delivery Stations. Since this algorithm will be implemented on a daily basis, it should be day of week aware. This means that the seasonality of the two forecasted outputs will affect the behaviour of the network.
A train set has been provided (train_data.csv) to train the model that will generate the forecast. Moreover, a test set has been added (test.csv) to predict on it and evaluate through submitting the predictions through Kaggle. The predictions will be for the entire month of July.

## Files in Repo
1. EDA : Basic Exploratory Data Analysis
2. Data Processor: Functions to pre process data (encode, cluster, ourlier management)
3. Prophet: Full Notebook to get predictions for Prophet with RMSE 366.60
4. Linear Regression: Full Notebook to get predictions for Linear Regression with RMSE 313.96
5. Lasso: Full Notebook to get predictions for Lasso with RMSE 278.17
6. Random Forrest: n/a with RMSE 303.75
7. Final Submission: Full Notebook to get predictions for XGBoost with RMSE 264.69
