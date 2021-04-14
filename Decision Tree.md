# Decision Tree
It makes decisions based on the conditions present in the data. It can give amazing results when the data is mostly categorical in nature and depends on conditions.

![image](https://user-images.githubusercontent.com/30498799/114527336-75ba0300-9c7a-11eb-9e9c-4a6825ecdc9b.png) 

In the above representation of a tree, the conditions such as the salary, office location and facilities go on splitting into branches until they come to a decision whether a person should accept or decline the job offer. The conditions are known as the internal nodes and they split to come to a decision which is known as leaf.

## Types of Decision Tree
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

## Advantages of Decision Tree
1.  _Preprocessing of data such as normalization and scaling is not required which reduces the effort in building a model._
2.  _It can handle both categorical and numeric data and is much efficient compared to other algorithms._
3.  _It's a flexible algorithm as it doesn't not affected by a missing value._


## Decision Tree Parameters
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


## Challenges in Decision Tree 
* **Overfitting**: Fatures with very low importnace can lead into overfitting of the model. This can be avoided by two methods
    1.  **_Pruning_**: It is a process of removing the branches having the features of low importance. It removes the nodes either from leaves or nodes. there are two pruning techniques such as post pruning and pre pruning used to avoid overfitting.
    2.  **_Ensemble method or bagging and boosting_** : It resamples the training data repeatedly by building multiple decision trees. Boosting technique is used to train new instances to give importance to those instances which are misclassified. AdaBoost is one commonly used boosting technique.
* **Discretization**: When the data contains too many numerical values, discretization is required as the algorithm fails to make a decision on such small and rapidly changing values. Such a process can be time consuming and produce inaccurate results when it comes in training the data.

#### If data contains too many logical conditions or is discretized to categories, then decision tree algorithm is the right choice. If the data contains too many numeric variables, then it is better to prefer other classification algorithms as decision tree will perform badly due to the presence of minute variation of attributes present in the data. Still, it is advisable to perform feature engineering on numeric data to confront the algorithm that a decision-making tree holds.
