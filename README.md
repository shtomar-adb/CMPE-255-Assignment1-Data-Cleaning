# CMPE-255 Assignment1 Data Cleaning  

Name: Shivam Tomar  
Email id: shivam.tomar@sjsu.edu  
Student id: 015218203  

## Files
- cmpe255_assignment1_data_cleaning.ipynb: jupyter notebook containing the assignment's python code
- AB_NYC_2019.csv: Dataset csv file downloaded from [Kaggle](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data  )

## Business Objective  
Predict the prices of airbnb rentals in NYC.

## Dataset used  
The dataset chosen for this assignment is the open dataset provided by Airbnb on the New York City Airbnb rentals in the year 2019.
URL to the dataset: https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data  

## Steps taken for cleaning the dataset and training the model
This assignment applies Linear Regression on the selected features of airbnb NYC dataset to create a regression model for predicting the airbnb rental prices. Before applying Linear Regression, dataset has been preprocessed and cleaned to make it suitable for creating accurate regression model.  
_Following steps were taken for preprocessing and cleaning dataset._  

#### 1). Label Encoding the columns with categorical values  
Following two features in the data set have categorical values:
- neigbourhood_group
- room_type
Label encode these two features using the scikit python package __LabelEncoder__

#### 2). Removing the non required features  
Following features doesn't add any value to the regression model trained for predicting the price and hence are removed.
- name
- id
- host_id
- host_name
- last_review
- neighbourhood

#### 3). Missing values handling  
Missing values of a feature are filled with the mean of remaining values of feature. Univariate approach has been taken for filling the missing values.  

#### 4). Separating Independent and Dependent features  
In this step all the features are splitted into two groups: Independent and Dependent. The independent features are used for training the Regression model to predict the Dependent feature.
##### Independent Features
- neighbourhood_group	
- latitude	
- longitude	
- room_type	
- minimum_nights	
- number_of_reviews	
- reviews_per_month	
- calculated_host_listings_count
- availability_365  
##### Dependent Feature
- price  

#### 5). Train Test Split  
The data points are then splitted into the Training and Testing data. 30% of the data points are allocated to testing data. Train test split is done by using _train_test_split_ Python function.

#### 6). Standardization of data  
Data is further standardized by python package __StandardScaler__

#### 7). Model Training
Finally the model is trained on Independent variable using _LinearRegression_ algorithm.

#### 8). R Squared score  
The R squared score of Regression model came out to be **12.071144240000532**






