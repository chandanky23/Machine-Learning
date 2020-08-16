# Calculating Linear function from sample data using Gradient Descent

In this notebook I am trying to deduce a linear function by using sample data set.
At every step I am trying to reduce the cost function (here to avoid negatives, taking mean squared error, MSE)

`cost = Y-Yi` and MSE takes the sqaure difference to remove negative values, incase if cost is negative

`MSE = (1/n)*sum((Y - Yi))^2`, n size of X and 0 >= i < n
also, `Yi = mXi + c`, where m stands for slope, c for intercept, n

* Taking a fixed learning rate and total number of Iterations.
* Taking a fixed value for slope and intercept to start with the dedcution

* At every Iteration doing derivative of the linear function (y = mx + c) with respect to:
  * m, where c = 0
  * c, where m = 0

* After this I am trying to calculate the new slope and intercept by utilising the learning rate and the derived data, i.e,
  formula:
    * `new slope = old slope - learning rate * d/dm of -(2/n) * sum(Xi*(Y-Yi))`, n size of X and 0 >= i < n
    * `new intercept = old intercept - learning rate * d/dc of -(2/n) * sum(Y-Yi)` n size of X and 0 >= i < n

* Finally with trial and error the loop provides the global minima slope and intercept once the previous MSE and the current MSE are same.

## Formula

`MSE = (1/n)*sum((Y - Yi))^2`, n size of X and 0 >= i < n
also, `Yi = mXi + c`, where m stands for slope, c for intercept, n

Assume learning rate,
`new slope = old slope - learning rate * d/dm of -(2/n) * sum(Xi*(Y-Yi))`, n size of X and 0 >= i < n
`new intercept = old intercept - learning rate * d/dc of -(2/n) * sum(Y-Yi)` n size of X and 0 >= i < n

## Required Data Set

From example tutorial
> math_cs_score.csv

## Prediction Data Set

Created the prediction set myself:
> math_cs_score_predicted_global_minima.csv

## Result Set

> slope for global minima

slope = 1.017738034475287

> intercept for global minima

intercept = 1.9150919894776326
