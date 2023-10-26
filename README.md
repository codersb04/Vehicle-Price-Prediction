# Vehicle-Price-Prediction
## Task
Build a machine learning model to predict prices of vehicle.</br>
Tool Used: Jupyter Notebook, Python</br>
Dataset: https://www.kaggle.com/datasets/toramky/automobile-dataset

## Steps Involved

### Importing Libraries:
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- train test split
- r2 score
- Linear Regression
- Lasso
- Random Forest Regressor
- cross val score
### Data Collection, Analysis and Processing:
- Load the csv file of dataset to pandas dataframe using read_csv function
- Use the function shape, describe and info function to understand the data better
- Create a list of all the numerical and categorical columns of the dataframe seperately
- Convert all the numerical column to int or float
- **Handling the missing value**
  - Replace all the missing values in numerical columns except price column to means of the respective columns
  - Drop the rows in which price value is missing
  - Replace the missing value in the categorical column with the mode of the column
- **Data Visualization**
  - Plot the Heatmap between the numerical column of the dataframe
  - Plot the histogram for the price column
    - The **graph can be seen as left skewed to convert it to normal distribution log function is used**.
    - log1p method is used which takes one parameter and returns the logarithm of the (number+1), i.e log(1+parameter)
    - Update the main dataframe with the new log value of price
  - Compare all the numerical column with the price column by plotting regplot
  - Compare all the Categorical Column with the price column by plotting Box plot
- **Data Processing**
  - Convert the categorical data into numerical form by using **get_dummie**s function
  - SPlit the dataframe into features and target
### Model Building and Evaluation
- Split the data into training and test set
- Model: Linear Regression
  - Accuracy score for training set:  0.9714588450225944
  - Accuracy score for test set:  0.9441825305802949
- Model: Lasso Regression
  - Accuracy score for training set:  0.8656167362348549
  - Accuracy score for test set:  0.7615021426228008
- Model: Random Forest Regressor
  - Accuracy score for training set:  0.9874175501585117
  - Accuracy score for test set:  0.9195192685003634
- Cross Validation Technique for model building and Evaluation:
  - Best Cross Validation Score is for Lasso Regression that is: 74.23
