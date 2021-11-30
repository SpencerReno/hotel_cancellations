# Hotel Cancellations

## Overview and Project Goal 
With this project, my goal was to predict whether or not a customer would cancel their stay at a hotel. The data used can be found [here](https://www.kaggle.com/jessemostipak/hotel-booking-demand). This dataset compared city hotels and resorts as their base two hotel types the data also included other features such as arrival dates, repeated guest, and their deposit types just to name a few. I used three classification models for the prediction process logistic regression, KneighborsClasifier, and XGBClassifier. 

## Cancellations based on average days on a waiting list
One clear point with this graph is that city hotels are stayed at more than resorts. Also, people who book a stay at a city hotel are more likely to sit on a waiting list longer than those at a resort hotel. After 4 days on a waiting list for a city hotel, it's likely the person is going to cancel their stay. For a resort hotel, it's even less on average people won't even wait one day on a waiting list for a resort hotel. This also could be due to them not having a large waiting list since those hotels are bigger than a normal city hotel, and can hold more people.

![avg days on waiting list](https://user-images.githubusercontent.com/88803320/143910927-45ef10d0-d127-4476-b0d6-8a7758c3b706.png)



## Number of Customers for each month
This graph could help out the hotels a lot as they can see where their strongest and weakest months are. During the summer their sales are very good in most cases this is due to people traveling for vacations and resort hotels are more based around the summertime. In order to increase sales in the winter, they could probably change a few things to increase the number of customers. People still travel during the winter seasons they just might not be looking for a resort feel or maybe their resorts aren't open during these times. Those are some key ideas they could look at to fix the lower numbers during the winter season. 

![number of customers](https://user-images.githubusercontent.com/88803320/143910911-68703d18-b10e-41c9-99bd-f7cf885cdee4.png)

## Number of Customers For each year 
similar to the graph before in comparing the months and the number of customers separated by the years. 2015 only shows from November to September but also had the lowest numbers of all three years. 2016 and 2017 both trade off frequently. However, as the years progressed it seemed as if the hotels were slowly starting to figure out how to increase their sales in the winter and early new year times. Taking note of what they did during October of 2016 and repeating that each year would really help a lot too as the month of October in 2016 was as high as the highest peak in 2017 of may.

![customers based on years and months](https://user-images.githubusercontent.com/88803320/143920394-a3f03cd7-ef5d-416d-a59b-46f141bfe600.png)


## Machine Learning Prediction Models
### KNeighborsClassifier
For my prediction models, I predicted the binary classification on whether or not a person is likely to cancel their stay or not. The first model I ran was a KNN Classification model that did very well. However, the run times were very long around two mins to complete.
![knn scores](https://user-images.githubusercontent.com/88803320/143914881-964859a9-02fc-4f22-a272-a8ee548bd973.JPG)


### XGBClassifier
Since the run time took a while I decided to go with an XGBClassifier to try and boost the testing scores up higher. With this model, I got a training and testing score of 1. To check for overfitting I predicted with all values in the X and made a new data frame with the predicted values and the actual Y values. Then a condiction column was added with all values set to False this is to check if the predicted values match the actual values. If the predicted value matched the actual value the condition would be changed from False to True. And checking the value counts on the condition column showed that there were no False values meaning that XGB was not overfitted and did predict all values correctly. 

![xgb scores](https://user-images.githubusercontent.com/88803320/143914899-8f0db4a2-9845-4583-a95f-cea637227cd5.JPG)


## PCA and LogisticRegression
Just to run one more model I ran a Logistic Regression model with PCA scaling. This model ran similar to the XGBClassifier with just a slight increase in run time. However, it had the same 1.0 training and testing scores for this model.

![logreg](https://user-images.githubusercontent.com/88803320/143915036-54dd8144-5de6-4e7a-bf0e-d04b9b33952c.JPG)
