# Hotel Cancellations

## Overview and Project Goal 
With this project my goal was to predict wheather or not a customer would cancel their stay at a hotel. The data used can be found [here](https://www.kaggle.com/jessemostipak/hotel-booking-demand). This dataset compared city hotels and resorts as their base two hotel types the data also inclued other features such as arrival dates, repeated guest, and their deposit types just to name a few. I used three classification models for the prediction process logistic regression, KneighborsClasifier, and XGBClassifier. 

## Cacellations based on average days on a waiting list
One clear point with this graph is that city hotels are stayed at more than resorts. Also, people who book a stay at a city hotel are more likly to sit on a waiting list longer than those at a resort hotel. After 4 days on a waiting list for a city hotel is likly when a person is going to cancel their stay. For a resort hotel is even less on average pepople wont even wait one day on a waiting list for a resort hotel. This also could be due to them not having a large waiting list since those hotels are bigger than a normal city hotel.



## Number of Customers for each month
This graph could help out the hotels a lot as they can see where their strongest and weakest months. During the summer their sales are very good in most cases this is due to people traveling for vacations and resort hotels are more based around the summer time. In order to increase sales in the winter they could probably change a few things to increase the number of customer. People still travel during the winter seasons they just might not be looking for a resort feel or maybe their resorts arent open during these times. Those are some key ideas they could look at to fixing the lower numbers during the winter season. 



## Machine Learning Prediction Models
### KNeighborsClassifier
For my prediction models I predicted the binary classification on whether or not a person is likly to cancel their stay or not. First model I ran was a KNN Classification model that did very well. However, the run times were very long around two mins to complete. 


### XGBClassifier
Since the run time took a while I decided to go with an XGBClassifier to try and boost the testing scores up higher. With this model I got a training and testing score of 1. To check for overfitting I predicted with all values in the X and made a new dataframe with the predicted values and the actual Y values. Then a condiction column was added with all values set to False this is to check if the predicted values match the actual values. If the predicted value matched the actual value the conition would be changed from False to True.
and checking the value counts on the condition column showed that there were no False values meaning that XGB was not over fit and actually did predict all values correct. 

## PCA and LogisticRegression
Just to run one more model I ran a logistic Regression model with pca scaling. This model ran similar to the XGBClassifier with just a slight increase in run time. However, it had the same 1.0 training and testing scores for this model.
