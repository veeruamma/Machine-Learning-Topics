# Machine-Learning-Topics

![image](https://user-images.githubusercontent.com/30498799/115365311-d73c1d80-a1f6-11eb-970f-a7151be8b9c6.png)


_**Bias**_ : Error generated on the training data 

_**Variance**_ : Error generated on the testing or unseen data 

## Underfitting and Overfitting

While fitting the model, there can be 2 events which will lead to the bad performance of the model. These events are
1. **Underfitting** : Where the model couldn't fit the data well enough. This model gives lower accuracy and is unbale to capture the relationship between input and output variables. It can be avoided by using more data or by optimising the parameters of the model.
**Higher Error on both train and test data i.e High Bias and High Variance**

2. **Overfitting** : When the model predicts very well on training data and is not able to predict well on test data or validation data. the main reason for this could be memorising the training data and unable to generalize the test or unseen data. It can be avoided by using regularisation techniques such as drop out or by propser features selection.
**Higher Error only on test data i.e Low Bias and High Variance**

![image](https://user-images.githubusercontent.com/30498799/114488493-0de8c580-9c44-11eb-801b-af238541efae.png)

## R-squared and Adjusted R-squard
In case of regression models, apart form the accuracy and loss, there are other metrics to evaluate the performance of the model such as R-squared and Adjusted R-squared.

**R-square may work well in simple linear regression but in case of multiple linear regression, every time you add a independent variable to the model, the R-Squared value increases, even if the independent variavle is insignificant. It never decreass. Whereas Adjusted R-squared values increases only when the independent variable is significant and affects dependent varibale .**

**Adjusted R-squared value will be always less than or equal to R-squared value** 

# The most popular Machine Learning Algorithms

## Linear Regression 

## Logistic Regression 

## Decision Tree

## Support Vector Machine(SVM) 

## Naive Bayes 

## K-nearest neighbour

## K-means 

## Random Forest

## Gradient Boosting algorithms
1.  GBM
2.  XGBoost
3.  LightGBM
4.  CatBoost

