# Food-Delivery-Time-Prediction

## Amazon Business Research Analyst Hiring Challenge

Size of training set: 45,593 csv files

Size of test set: 11,399 csv files

## Features
![image](https://user-images.githubusercontent.com/88038908/187479780-20168ca1-ce3f-4797-8fa8-a7beaa90573d.png)

![image](https://user-images.githubusercontent.com/88038908/187479962-46949afb-288f-4ada-9d00-7c924d19c87d.png)

## Data Analysis and Processing

- First individual CSV files are read and stored as a records in a single dataframe.
- From the above features we dropped 'Name:','ID','Delivery_person_ID','Type_of_order',Order_Date' because it doesn't affect the delivery time.
- 
### Feature Engineering
- We added new feature called "distance" which is the calculated result of the distance between restaurent and delivery location and we dropped latitute and longitude columns ('Restaurant_latitude','Restaurant_longitude','Delivery_location_latitude','Delivery_location_longitude')
- we added new feature called "Preparation Time" which is the amount of time (in Min) it took from the order received to order picked by delivery guy and we dropped 'Time_Order_picked','Time_Order' columns.
- we used one hot encode representation of few features.


### Training 
- We trained the data with multiple Machine Learning models such as linear regression, SVR, Decision tree regression and Deep learning ANN model.
- We got the best r2 score of 88 for ANN model (from labeled data)
- for better test score we re-trained the model with complete train data without spliting it into train,test and validation data and we are able to increase test score by 5 points from 78 to 83 for test data.

