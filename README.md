# google_playstore_predictions

We want to look into three key areas at this stage:
1. Find the size range in which the most numbers of installs are obtained for an app in different categories
2. Predict the Average User Rating an app would get, based on the features like category, price, and size
3. Predict the number of total installs an app would get, based on the features like category, price, and size


Main findings and Results
Through the various experiments we found out how to properly clean the dataset, specifically convert the datatypes of important features and make them suitable for regression. 
Through the various explorative analyses and the pandas profiling, we got many inferences about the data including correlations
The first main finding is that we found out the best app size ranges for getting the maximum number of installs in different categories. 

Category
Minimum Size
Maximum Size
Best Size Range to get Maximum Installs
Adventure
0.045 MB
1100 MB
800-900 MB
Maps & Navigation
0.016 MB
382 MB
150-200 MB
Role Playing
0.043 MB
1500 MB
1000-1200 MB


Figure 6. Best Size range in different categories
 
Then using various regression models we were able to predict the rating and number of installs
We chose the linear regression as the baseline and calculated the MSE and MAE for it
We then conducted various other regressions and found the model with the least error.  We found that for predicting the Ratings, the Random Forest Regressor provided the best predictions and the least error

Predicting App Ratings

Regression
MSE
MAPE
Linear (Baseline)
4.221
4354160987210370.0
Random Forest
0.4
0.07
Bayesian ARD
2.058
4369784657954465.5
Bayesian ridge
2.054
4354193448350276.5
Linear SVR
2.508
3135247702318329.5
Epsilon SVR
Taking too much time to fit
Taking too much time to fit


Figure 7. Results from multiple regression models
 
While predicting the Number of Installs we found that the error rate was quite high in all the regressors
We found that the Epsilon SVR is not suitable for our particluar dataset

