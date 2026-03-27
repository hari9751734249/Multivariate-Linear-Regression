# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner


## Algorithm:

Step 1: Import the necessary libraries, pandas for data manipulation and linear_model from sklearn for the regression algorithm.

Step 2: Load the dataset from the CSV file and separate the independent variables (Weight and Volume) as X and the dependent variable (CO2) as y.

Step 3: Create a linear regression model instance and train it by fitting it with the X and y data.

Step 4: Extract and print the model's calculated coefficients and the y-intercept.

Step 5: Provide a new set of input values for Weight and Volume, use the trained model to predict the CO2 emission, and print the final prediction.


## Program:
```
import pandas as pd

from sklearn import linear_model

df = pd.read_csv("carsemission.csv")

X = df[['Weight', 'Volume']]

y = df['CO2']

regr = linear_model.LinearRegression()

regr.fit(X, y)

print('Coefficients:', regr.coef_)

print('Intercept:', regr.intercept_)

input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})

predictedCO2 = regr.predict(input_data)

print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:

<img width="1363" height="388" alt="image" src="https://github.com/user-attachments/assets/11fdd336-1d42-48e7-9896-001416471bfe" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
