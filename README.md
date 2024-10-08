# Predicting-Movie-Rental-Durations
Build a regression model for a DVD rental firm to predict rental duration. Evaluate models to recommend the best one.

# Description: 
Time to put your regression knowledge to the test! A DVD rental company has approached you to make a regression model which will help predict the number of days a customer rents a DVD. The model will hopefully make their inventory planning much more efficient. You decide to help them by running some regression models and recommending the best-performing model to the company.

# Project Instructions
In this project, you will use regression models to predict the number of days a customer rents DVDs for.

As with most data science projects, you will need to pre-process the data provided, in this case, a csv file called rental_info.csv. Specifically, you need to:

Read in the csv file rental_info.csv using pandas.
Create a column named "rental_length_days" using the columns "return_date" and "rental_date", and add it to the pandas DataFrame. This column should contain information on how many days a DVD has been rented by a customer.
Create two columns of dummy variables from "special_features", which takes the value of 1 when:
The value is "Deleted Scenes", storing as a column called "deleted_scenes".
The value is "Behind the Scenes", storing as a column called "behind_the_scenes".
Make a pandas DataFrame called X containing all the appropriate features you can use to run the regression models, avoiding columns that leak data about the target.
Choose the "rental_length_days" as the target column and save it as a pandas Series called y.
Following the preprocessing you will need to:

Split the data into X_train, y_train, X_test, and y_test train and test sets, avoiding any features that leak data about the target variable, and include 20% of the total data in the test set.
Set random_state to 9 whenever you use a function/method involving randomness, for example, when doing a test-train split.
Recommend a model yielding a mean squared error (MSE) less than 3 on the test set

Save the model you would recommend as a variable named best_model, and save its MSE on the test set as best_mse.


![image](https://github.com/user-attachments/assets/49a4e2b2-a5e8-445d-a329-618f787a1e58)


A DVD rental company needs your help! They want to figure out how many days a customer will rent a DVD for based on some features and has approached you for help. They want you to try out some regression models which will help predict the number of days a customer will rent a DVD for. The company wants a model which yeilds a MSE of 3 or less on a test set. The model you make will help the company become more efficient inventory planning.

The data they provided is in the csv file `rental_info.csv`. It has the following features:
- `"rental_date"`: The date (and time) the customer rents the DVD.
- `"return_date"`: The date (and time) the customer returns the DVD.
- `"amount"`: The amount paid by the customer for renting the DVD.
- `"amount_2"`: The square of `"amount"`.
- `"rental_rate"`: The rate at which the DVD is rented for.
- `"rental_rate_2"`: The square of `"rental_rate"`.
- `"release_year"`: The year the movie being rented was released.
- `"length"`: Lenght of the movie being rented, in minuites.
- `"length_2"`: The square of `"length"`.
- `"replacement_cost"`: The amount it will cost the company to replace the DVD.
- `"special_features"`: Any special features, for example trailers/deleted scenes that the DVD also has.
- `"NC-17"`, `"PG"`, `"PG-13"`, `"R"`: These columns are dummy variables of the rating of the movie. It takes the value 1 if the move is rated as the column name and 0 otherwise. For your convinience, the reference dummy has already been dropped.

