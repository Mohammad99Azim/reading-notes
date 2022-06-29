# Linear Regression

Linear regression analysis is used to predict the value of a variable based on the value of another variable. The variable you want to predict is called the dependent variable. The variable you are using to predict the other variable's value is called the independent variable.

### When Do You Need Regression?

- you need regression to answer whether and how some phenomenon influences the other or how several variables are related
- Regression is also useful when you want to forecast a response using a new set of predictors.

#### Linear Regression

Linear regression is probably one of the most important and widely used regression techniques. It’s among the simplest regression methods. One of its main advantages is the ease of interpreting results.


## Python Packages for Linear Regression

 -  NumPy 
 -  scikit-learn : is a widely used Python library for machine learning, built on top of NumPy and some other packages.
 -  statsmodels. It’s a powerful Python package for the estimation of statistical models, performing tests, and more

install all these packages into a virtual environment:
  ``python -m pip install numpy scikit-learn statsmodels``


## Simple Linear Regression With scikit-learn

### Step 1: Import packages and classes:

```
import numpy as np
from sklearn.linear_model import LinearRegression
```

### Step 2: Provide data

```
x = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1))
y = np.array([5, 20, 14, 32, 22, 38])
```
 You should call .reshape() on x because this array must be two-dimensional, or more precisely, it must have one column and as many rows as necessary.

the x and y should be liket this 


```
>>> x
array([[ 5],
       [15],
       [25],
       [35],
       [45],
       [55]])

>>> y
array([ 5, 20, 14, 32, 22, 38])
```
As you can see, x has two dimensions, and x.shape is (6, 1), while y has a single dimension, and y.shape is (6,).

### Step 3: Create a model and fit it

```
model = LinearRegression()
```
This statement creates the variable model as an instance of LinearRegression. You can provide several optional parameters but here we will use the defult

It’s time to start using the model. First, you need to call .fit() on model:

```
model.fit(x, y)
```
With .fit(), you calculate the optimal values of the weights 𝑏₀ and 𝑏₁, using the existing input and output, x and y, as the arguments. In other words, .fit() fits the model. It returns self, which is the variable model itself. That’s why you can replace the last two statements with this one:

```
model = LinearRegression().fit(x, y)
```

### Step 4: Get results

Once you have your model fitted, you can get the results to check whether the model works satisfactorily and to interpret it.

You can obtain the coefficient of determination, 𝑅², with .score() called on model:

```
>>> r_sq = model.score(x, y)
>>> print(f"coefficient of determination: {r_sq}")
coefficient of determination: 0.7158756137479542
```

When you’re applying .score(), the arguments are also the predictor x and response y, and the return value is 𝑅².

The attributes of model are .intercept_, which represents the coefficient 𝑏₀, and .coef_, which represents 𝑏₁:

```
>>> print(f"intercept: {model.intercept_}")
intercept: 5.633333333333329

>>> print(f"slope: {model.coef_}")
slope: [0.54]

```
The code above illustrates how to get 𝑏₀ and 𝑏₁. You can notice that .intercept_ is a scalar, while .coef_ is an array.


### Step 5: Predict response

To obtain the predicted response, use .predict():
```
>>> y_pred = model.predict(x)
>>> print(f"predicted response:\n{y_pred}")
predicted response:
[ 8.33333333 13.73333333 19.13333333 24.53333333 29.93333333 35.33333333]
```

In this case, you multiply each element of x with model.coef_ and add model.intercept_ to the product.

