# Logistic Regression

It solely depends on maximum likelihood estimation. _Maximum likelihood estimation maximises the probability that classifies the event being 1 or 0 by estimating certain parameters. Every probability equation goes by the following._

![image](https://user-images.githubusercontent.com/30498799/114493582-61134600-9c4d-11eb-8376-8dd566a62081.png)

It finds out the probability by transforming the dependent/predictive variable  into a logit variable with respect to the independent/input variable or the features of the input data.

#### Merits of Logistic Regression
  * Logistic Regression has less chance of overfitting.
  * Tuning of parameters is not required much

#### Merits of Logistic Regression
  * They fail to play good in large datasets
  * The algorithm **only works fine in linearly separable data**
  * They are not flexible with continuous data

##### Logistic Regression works fine only when the target variable is discrete in nature. They do not have the flexibility to act as regression analysis. Also, they have less chance of overfitting but in data having a higher dimension, logistic can overfit. For such cases, there are regularising techniques called L1 and L2 which shrink the coefficients of the algorithm to avoid overfitting.  Logistic regression can also work fine with the discretised data as they do not follow a decision-based approach.


It is basically used for binary classification. But why does it call as regression ??? It's because as the no of outliers increses the best fit line deviates from the originality and causes wrong predictions.
Hence to deal with outliers, a function called Sigmoid is used in Logistic Regression, which gives values between 0 and 1 by removing the outliers and it's defined as 


![image](https://user-images.githubusercontent.com/30498799/115192640-a76d1700-a11d-11eb-9d87-bf48f5dbec75.png) 


The plot of the Sigmoid function will be S curve as shown below

![image](https://user-images.githubusercontent.com/30498799/115192766-d5525b80-a11d-11eb-9b1f-ab4213dd78ef.png)


Can we also solve multi class classfication ? The naswer is yes, we can use ot for multi class classification also. It's also known as One v/s Rest (ALL).  It will group the few of all the categories as one category and rest as other category and builds a model. Similarly it will go for all the combinations of categories and try to learn and predict the multiple categories. The probabilities given by multiple models will be chosen by the maximum value as the output.
