
# Real Estate - Price Predictor

# 1. Business Problem

## 1.1 Problem Context
Our client is a large Real Estate Investment Trust (REIT).

* They invest in houses, apartments, and condos(complex of buildings).
* As part of their business, they try to predict the fair transaction price of a property before it's sold.
* They do so to calibrate their internal pricing models and keep a pulse on the market.

Sources: 


    (a) Origin:  This dataset was taken from the StatLib library which is
        maintained at Carnegie Mellon University.
    (b) Creator:  Harrison, D. and Rubinfeld, D.L. 'Hedonic prices and the 
        demand for clean air', J. Environ. Economics & Management,
        vol.5, 81-102, 1978.
    (c) Date: July 7, 1993

## 1.2 Problem Statement

* The REIT has hired us to find a data-driven approach to valuing properties.
* They currently have an untapped dataset of transaction prices for previous properties on the market.
* Our task is to build a real-estate pricing model using that dataset.
* If we can build a model to predict transaction prices with an average error, then our client will be very satisfied with the our resultant model.

## 1.3 Business Objectives and Constraints

* Deliverable: Trained model file
* Model Interpretability will be useful
* No latency requirement

# 2. Machine Learning Problem

## 2.1 Data Overview

* Concerns housing values in suburbs of Boston.
* Number of Instances: 506
* Number of Attributes: 13 continuous attributes (including "class"
                      attribute "MEDV"), 1 binary-valued attribute.

## Features of the data


    1. CRIM      per capita crime rate by town
    2. ZN        proportion of residential land zoned for lots over 
                 25,000 sq.ft.
    3. INDUS     proportion of non-retail business acres per town
    4. CHAS      Charles River dummy variable (= 1 if tract bounds 
                 river; 0 otherwise)
    5. NOX       nitric oxides concentration (parts per 10 million)
    6. RM        average number of rooms per dwelling
    7. AGE       proportion of owner-occupied units built prior to 1940
    8. DIS       weighted distances to five Boston employment centres
    9. RAD       index of accessibility to radial highways
    10. TAX      full-value property-tax rate per $10,000
    11. PTRATIO  pupil-teacher ratio by town
    12. B        1000(Bk - 0.63)^2 where Bk is the proportion of blacks 
                 by town
    13. LSTAT    % lower status of the population
    14. MEDV     Median value of owner-occupied homes in $1000's


# 2.2 Mapping business problem to ML problem
##  2.2.1 Type of Machine Learning Problem

It is a regression problem, where given the above set of features, we need to predict the transaction price of the house.

## 2.2.2 Performance Metric (KPI)
Since it is a regression problem, we will use Root Mean Squared Error (RMSE)