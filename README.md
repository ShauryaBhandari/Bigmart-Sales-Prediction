# Bigmart-Sales-Prediction
Solution of the Bigmart Sales Prediction problem by Analytics Vidhya
### Problem Statement 		  
The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined. The aim is to build a predictive model and find out the sales of each product at a particular store.

Using this model, BigMart will try to understand the properties of products and stores which play a key role in increasing sales.


## The Data
We have train (8523) and test (5681) data set consisting of 12 features, train data set has both input and output variable(s) We need to predict the sales for test data set.

Variable | Description
----------|--------------
Item_Identifier | Unique product ID
Item_Weight | Weight of product
Item_Fat_Content | Whether the product is low fat or not
Item_Visibility | The % of total display area of all products in a    store allocated to the particular product
Item_Type | The category to which the product belongs
Item_MRP | Maximum Retail Price (list price) of the product
Outlet_Identifier | Unique store ID
Outlet_Establishment_Year | The year in which store was established
Outlet_Size | The size of the store in terms of ground area covered
Outlet_Location_Type | The type of city in which the store is located
Outlet_Type | Whether the outlet is just a grocery store or some sort of supermarket
Item_Outlet_Sales | Sales of the product in the particulat store. This is the outcome variable to be predicted.


### Why does the the problem need to be solved?

I’m building this model for my own learning purposes. It should provide a good insight in what drives the sales for a products.
This is an easily scalable model to provide detailed info and accurate predictions for sales volume for different type of products as there is a lot of data out there.
This solution can be used for projects, start-ups and sales forecast.

### How would I solve the problem?

I would find the sales data for a product as detailed as possible (with as many features as possible). Select all the features with no NaN or missing data. Select the obviously important features for the model. All the other put them aside as we will be experimenting with them. Visualize the data (read through it and build some scatter, history plots for linearity and dimensionality and box plots for outliers).
Build the model with different algorithms starting with the simplest and moving up to more complicated. Evaluate the performance of each algorithm. Try combining 2-3 of them and evaluate the new performance. Choose the best model and deploy it on all the test data you can find.

### What I did:
1. Replaced the Nans and zero values, identified outliers, feature selection and normalization - for both train and test data.
2. Visualised the data, studied the correlation amongst the data and chose the required features.
3. Built the models: I created a single model function to which I passed various different models such as Linear Regression, Decision Trees and Random Forests. I will soon be adding tree boosting to it as well.
4. Calculated the Root Mean Squared Error (RMSE), predicted the sales, cross validated the scores.
5. Classified the train data and imported the results for respective machine learning models to separate csv files (which have been attached above). The Decision Tree algorithm proved to be a clear winner with the lowest RMSE value.
