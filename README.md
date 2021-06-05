# Background of Problem Statement :
The US Census Bureau has published California Census Data which has 10 types of metrics such as the population, median income, median housing price, and so on for each block group in California. The dataset also serves as an input for project scoping and tries to specify the functional and nonfunctional requirements for it.

# Problem Objective :
The project aims at building a model of housing prices to predict median house values in California using the provided dataset. This model should learn from the data and be able to predict the median housing price in any district, given all the other metrics.
Districts or block groups are the smallest geographical units for which the US Census Bureau publishes sample data (a block group typically has a population of 600 to 3,000 people). There are 20,640 districts in the project dataset.

# Domain: Finance and Housing.

# Analysis Tasks performed:
1.Built a model of housing prices to predict median house values in California using the provided dataset.

2.Trained the model to learn from the data to predict the median housing price in any district, given all the other metrics.

3.Predicted housing prices based on median_income and plot the regression chart for it.

# Requirements:
We need jupyter notebook environment for executing python program.

# Packages and libraries required:
•Pandas

•Numpy

•Matplotlib

•Scikit learn

•Seaborn

# Reading the data:
I imported the raw data which is in csv format from local database using pandas library.

# Dataset Description:


           Field                                Description
         
longitude	(signed numeric - float) : Longitude value for the block in California, USA


latitude	(numeric - float ) : Latitude value for the block in California, USA


housing_median_age	(numeric - int ) : Median age of the house in the block


total_rooms	(numeric - int ) : Count of the total number of rooms (excluding bedrooms) in all houses in the block


total_bedrooms	(numeric - float ) : Count of the total number of bedrooms in all houses in the block


population	(numeric - int ) : Count of the total number of population in the block


households	(numeric - int ) : Count of the total number of households in the block


median_income	(numeric - float ) : Median of the total household income of all the houses in the block


ocean_proximity	(numeric - categorical ) : Type of the landscape of the block [ Unique Values : 'NEAR BAY', '<1H OCEAN', 'INLAND', 'NEAR OCEAN', 'ISLAND'  ]


median_house_value	(numeric - int ) : Median of the household prices of all the houses in the block

# Data Visualization:
Distribution of the independent variables using hist() function from matplotlib library.


![](https://github.com/Dany511/Dany5_portfolio/blob/main/images%202/hist_1.PNG) ![](https://github.com/Dany511/Dany5_portfolio/blob/main/images%202/hist_2.PNG)

# Correlation Heat map:
Used sns.heatmap() function from seaborn library to visualize the Correlation heat map for the total dataset.


![](https://github.com/Dany511/Dany5_portfolio/blob/main/images%202/Corr_1.PNG)

# Handling the missing values: 
Used info() function to find the missing values.And all the missing values are taken care by replacing the missing values with the mean of their respective column using SimpleImputer() function.

# Encoding of categorical values: 
To know the data type of columns , we use dtypes function to get the columns with object data type and encoded them using get_dummies function from Pandas library.

# Standardisation of data: 
I have to standardize the data because the features of data have different range of values. I standardized the data using StandardScaler from Sklearn.

# Splitting of data:
I have split  80% of the total data into training dataset(x_train,x_test) and 20% of the total data into test dataset(y_train,y_test).

# Model Training and Model Testing: 
The training data is fed to LinearRegression by using fit() function, after training the model i used test data to predict the values of housing price using predict() function.

# Model Evaluation:
For evaluating the model i have calculated Mean_Squared_Error and R-Squared value.

•MSE=69710.078

•R2=0.65

# Linear Regression with one independent variable :
•Extracted just the median_income column from the independent variables (from X_train and X_test).


•Perform Linear Regression to predict housing values based on median_income.


•Predicted output for test dataset using the fitted model.


•Made a Plot of fitted model for training data as well as for test data to check if the fitted model satisfies the test data.


# Plot of Actual vs Predicted values:
                                   Actual vs Predicted (Training Data)
                                         
                                         
   ![](https://github.com/Dany511/Dany5_portfolio/blob/main/images%202/actual%20vs%20pred%20train.PNG)
   
   
   
                                   Actual vs Predicted (Test Data)
                                   
   ![](https://github.com/Dany511/Dany5_portfolio/blob/main/images%202/actual%20vs%20pred%20test.PNG)                                

# Conclusion:
In the above plot we can see that Actual vs Predicted values of both Training data and Test data follows a linear pattern.From this we can conclude that the fitted model satifies the test data.



