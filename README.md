# Machine-Learning-Topics
Projects worked on machine learning algorithms

## Underfitting and Overfitting

While fitting the model, there can be 2 events which will lead to the bad performance of the model. These events are
1. **Underfitting** : Where the model couldn't fir the data well enough. This model gives lower accuracy and is unbale to capture the relationship between input and output variables. It can be avoided by using more data or by optimising the parameters of the model.
2. **Overfitting** : When the model predicts very well on training data and is not able to predict well on test data or validation data. the main reason for this could be memorising the training data and unable to generalize the test or unseen data. It can be avoided by using regularisation techniques such as drop out or by propser features selection.

![image](https://user-images.githubusercontent.com/30498799/114488493-0de8c580-9c44-11eb-801b-af238541efae.png)


## Linear Regression 
It is a method used to find the relationship between the outcome variable also known as the dependent variable, and one or more variable often called as independent variables. This method is mostly used for forecasting. There are different rehression techniques based on the number of independent varibales and the type of realtionship between varibales.

Regression 
* Performed when the type of dependent or target varibale is continuous and independent variable could be continuous or categorical or nominal. 
* Tries to find the best fit line, which shows the relationship between dependent and independent variables with least error.

**The impact of change in independent varibales on the dependent variable can be described using the best fit line.**

Best fit line equation for linear regression is **y= mx + c**,  where m is slope and c is intercept or constant

#### Simple Linear Regression : If there is only input/independent varibale. y = mx + c, trying to find the best m and c values for y and x. Just a line
#### Multiple Linear Regression : If there are more than one input/independent varibale. y = m1x1 + m2x2 + ... +c, trying to find the best set of m and c values. It's a plane

![image](https://user-images.githubusercontent.com/30498799/114487189-c06b5900-9c41-11eb-8278-c3a77dd6a158.png)


### Assumptions for Linear Regression models
1. Linearity : should have linear relationship b/w input and output variables.
2. Multicollinearity : two or more input variables shouldn't be highly correlated
3. Homoscedasticity : residuals should be homoscedasticity that means variance of error are constant across input variables
4. Multivariate Normality : residuals should be normally distributed.
5. Categorical data : categorical data should be converted into dummy variables.
6. Minimum records : at least of 20 records of input variables needed.

#### Polynomial Regression : It is a non-linear regression and relationship of output variable is fitted to nth degree of the input variable.

#### Advantages of Using Linear Regression
1.  Linear Regression method is very easy to use. If the relationship between the variables (independent and dependent) is known, we can easily implement the regression method accordingly (Linear Regression for linear relationship).
2.  Linear Regression provides the significance level of each attribute contributing to the prediction of the dependent variable. With this data, we can choose between the variables which are highly contributing/ important variables. 
3.  After performing linear regression we get the best fit line, which is used in prediction, which we can use according to the business requirement.

#### Limitations of Linear Regression
 1. The main limitation of linear regression is that its performance is not up to the mark in the case of a nonlinear relationship.
 2. Linear regression can be affected by the presence of outliers in the dataset.
 3. The presence of high correlation among the variables also leads to the poor performance of the linear regression model.

## Logistic Regression 
It solely depends on maximum likelihood estimation. _Maximum likelihood estimation maximises the probability that classifies the event being 1 or 0 by estimating certain parameters. Every probability equation goes by the following._

![image](https://user-images.githubusercontent.com/30498799/114493582-61134600-9c4d-11eb-8376-8dd566a62081.png)

It finds out the probability by transforming the dependent/predictive variable  into a logit variable with respect to the independent/input variable or the features of the input data.

#### Merits of Logistic Regression
  * Logistic Regression has less chance of overfitting.
  * Tuning of parameters is not required much

#### Merits of Logistic Regression
  * They fail to play good in large datasets
  * The algorithm only works fine in linearly separable data
  * They are not flexible with continuous data

##### Logistic Regression works fine only when the target variable is discrete in nature. They do not have the flexibility to act as regression analysis. Also, they have less chance of overfitting but in data having a higher dimension, logistic can overfit. For such cases, there are regularising techniques called L1 and L2 which shrink the coefficients of the algorithm to avoid overfitting.  Logistic regression can also work fine with the discretised data as they do not follow a decision-based approach.

## Decision Tree
It makes decisions based on the conditions present in the data. It can give amazing results when the data is mostly categorical in nature and depends on conditions.

![image](https://user-images.githubusercontent.com/30498799/114527336-75ba0300-9c7a-11eb-9e9c-4a6825ecdc9b.png) 

In the above representation of a tree, the conditions such as the salary, office location and facilities go on splitting into branches until they come to a decision whether a person should accept or decline the job offer. The conditions are known as the internal nodes and they split to come to a decision which is known as leaf.

### Types of Decision Tree
1.  **Classification** : These trees are applied on data when the outcome is discrete in nature or is categorical such as a person died or survived, approval of loan etc.
2.  **Regression** : These trees are used when the outcome of the data is continuous in nature such as prices, age of a person, length of stay in a hotel, etc.

There are different types of algorithms used to build decision tree such as
1.  **Iterative Dichotomiser 3 (ID3)** :
   * It generates a tree by considering the whole set S as the root node then iterates and splits the data into subsets to calculate the entropy.
   * It is harder to use on continuous data and splitting the data in case of continuous data is time consuming

2. **C4.5**:
   * It's quite advanced compared to ID3 as it considers the data which are classified samples.
   * It generates a tree by splitting samples based on the normalized information gain and the feature having the highest information gain makes the decision.
   * it can handle both continuous and discrete attributes
   * It removes all the branches having low importance.
   
3. **Classification And Regression Tree CART**:
   * It can perform both classification and regression tasks.
   * It generates tree by considering Gini index.
   * It follows Greedy algorithm for splitting thus reduce the cost function. 
   * For classification, Gini index is used as cost function
   * For regression, sum squarred error is used as cost function
   
5. **Chi-square Automatic Interaction Detector (CHAID)**:
   * It can deal with any type of variables such as nominal, ordinal or continuous.
   * In regression tree, it uses F-test and in classification trees, it uses the Chi-Square test.
   * It is very less used and adopted in real world problems compared to other algorithms.
  
7. **Multivariate adaptive regression splines (MARS)**: It is implemented in regression problems when the data is mostly nonlinear in nature.

#### Advantages of Decision Tree
1.  _Preprocessing of data such as normalization and scaling is not required which reduces the effort in building a model._
2.  _It can handle both categorical and numeric data and is much efficient compared to other algorithms._
3.  _It's a flexible algorithm as it doesn't not affected by a missing value._


#### Decision Tree Parameters
1.  **Entropy** :
    * It is a measure of impurity present in the data.
    * Entropy with the lowest value makes a model better in terms of prediction as it segregates the classes better.

2.  **Information Gain** :
    * It is a measure used to generalize the impurity.
    * Higher the information gain, lower is the entropy.
    * 
3.  **Gini** :
    * It is a measure of misclassification and is used when the data contain multi class labels.
    * It is similar to entropy but it calculates much quicker than entropy.
  
4.  **Reduction in Variance** :
    * It is used when the decision tree works for regression and the output is continuous is nature.


#### Challenges in Decision Tree 
* **Overfitting**: Fatures with very low importnace can lead into overfitting of the model. This can be avoided by two methods
    1.  **_Pruning_**: It is a process of removing the branches havign the features of low importance. It removes the nodes either from leaves or nodes. there are two pruning techniques such as post pruning and pre pruning used to avoid overfitting.
    2.  **_Ensemble method or bagging and boosting_** : It resamples the training data repeatedly by building multiple decision trees. Boosting technique is used to train new instances to give importance to those instances which are misclassified. AdaBoost is one commonly used boosting technique.
* **Discretization**: When the data contains too many numerical values, discretization is required as the algorithm fails to make a decision on such small and rapidly changing values. Such a process can be time consuming and produce inaccurate results when it comes in training the data.

##### If data contains too many logical conditions or is discretized to categories, then decision tree algorithm is the right choice. If the data contains too many numeric variables, then it is better to prefer other classification algorithms as decision tree will perform badly due to the presence of minute variation of attributes present in the data. Still, it is advisable to perform feature engineering on numeric data to confront the algorithm that a decision-making tree holds.


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

