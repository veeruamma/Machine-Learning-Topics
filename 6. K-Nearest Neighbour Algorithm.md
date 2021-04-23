# K-Nearest Neighbour Algorithm

KNN belongs to a group of lazy learners where as logistic, SVM, Neural Nets belong to Eager Learners. Lazy learners store the training data in memory and arranges the data in order to find the closest neighbours efficiently during the inference phase. Otherwise, it will have to compare every new case with whole dataset making it quite inefficient.

**Eager Learners :** During the training phase, the algorithm tries learn the best fit line that need a lot computations and take a lot of time.
**Lazy Learners :** They don't involve many computations and hence train much faster.

The k-nearest neighbors algorithm (k-NN) is a non-parametric method used for classification and regression.[1] In both cases, the input consists of the k closest training examples in the feature space. The output depends on whether k-NN is used for classification or regression:

In k-NN classification, the output is a class membership. An object is classified by a plurality vote of its neighbors, with the object being assigned to the class most common among its k nearest neighbors (k is a positive integer, typically small). If k = 1, then the object is simply assigned to the class of that single nearest neighbor.
In k-NN regression, the output is the property value for the object. This value is the average of the values of k nearest neighbors.


### How K-NN works ?
(Classification example)
1.  Select K value
2.  Calculate the distance of K no of nearest neighbours.
3.  How many nearest belong to each category
4.  Finally, the classification is done based on maximum no of neighbours of the cteagories found.


(Regression example)
1.  Select K value
2.  Calculate the mean or average distance of K no of nearest neighbours and predicts the value.

Metrics such as Ecludian, Manahattan distance calculations are used to find the nearest neighbours.

In case of imbalanced dataset and outliers, the KNN can be biased w.r.t output.

Choosing the K-value for KNN is trcicky and it's selected using the error rate behaviour w.r.t the K value. This selection can help in getting the robust model.
