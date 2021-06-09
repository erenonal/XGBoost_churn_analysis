# Churn Classification Project

#### Retention of users is very important in companies, websites or telecommunication companies. Involving potential customers in our company, attracting customers who are considering leaving, or identifying customers that we cannot keep no matter what we do and not investing more will return us positive in terms of efficiency.For these reasons, churn analysis allows us to take action in advance and improve our marketing and investment techniques in this direction.

# Applications

I made classification with `XGBoost` algorithm using a ready dataset.

The explanations of the codes are also written as a comment line in detail, but I will write the operations I have done.

After defining the libraries we use, we read our file. I defined the reading patterns for the colab environment and for the local environment.

To familiarize yourself with the dataset, we took a look at the variable names and types.

After changing the type of the `TotalCharges` variable from object to float64, we removed the unnecessary columns.

I used the dummies method to convert categorical variables to numeric variables. Before doing this, I converted some variables to 0-1 values to be able to express them with a single variable to avoid unnecessary increase in the number of columns.

After looking at the correlation states I drop the ineffective variables

In order to better understand the data set, I analyzed the gender, retirement, contract duration, service status and churn status on graphs.

And now we can move on to the modeling phase.

I used the `MinMaxScaler` method to scale. I set the scaling range to 0 and 1 . I split the train-test dataset as 70%-30%

I used the best_params method to find the best fit values for the model and set the optimal hyperparameters. I ran my model paying attention to the Accuracy value and got an `accuracy score as 80%`.

Finally, I plotted the complex matrix graphically.

# Required Libraries

* `pandas`  (load and manipulate data and for One-Hot Encoding)

* `numpy`  (calculate the mean and standard deviation)

* `xgboost` (XGBoost stuff)

* `seaborn` (some graphs)

* `sklearn.model_selection` , train_test_split (split  data into training and testing sets)

* `sklearn.model_selection` , GridSearchCV (cross validation)

* `sklearn.metrics` , confusion_matrix (creates a confusion matrix)

* `sklearn.metrics` , plot_confusion_matrix (draws a confusion matrix)

* `matplotlib.pyplot`

* `matplotlib.ticker`  (for specifying the axes thick format)

* `io` (reading files for all systems)


# About Dataset

#### The data contains information about almost 6000 users, their demographic characteristics, the services they use, the duration of using the operator's services, the method of payment, and the amount of payment. Features are showing below.


customerID - customer id

gender - client gender (male / female)

SeniorCitizen - is the client retired (1, 0)

Partner - is the client married (Yes, No)

tenure - how many months a person has been a client of the company

PhoneService - is the telephone service connected (Yes, No)

MultipleLines - are multiple phone lines connected (Yes, No, No phone service)

InternetService - client's Internet service provider (DSL, Fiber optic, No)

OnlineSecurity - is the online security service connected (Yes, No, No internet service)

OnlineBackup - is the online backup service activated (Yes, No, No internet service)

DeviceProtection - does the client have equipment insurance (Yes, No, No internet service)

TechSupport - is the technical support service connected (Yes, No, No internet service)

StreamingTV - is the streaming TV service connected (Yes, No, No internet service)

StreamingMovies - is the streaming cinema service activated (Yes, No, No internet service)

Contract - type of customer contract (Month-to-month, One year, Two year)

PaperlessBilling - whether the client uses paperless billing (Yes, No)

PaymentMethod - payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))

MonthlyCharges - current monthly payment

TotalCharges - the total amount that the client paid for the services for the entire time

Churn - whether there was a churn (Yes or No)


Here is the link for dataset : https://www.kaggle.com/radmirzosimov/telecom-users-dataset







































