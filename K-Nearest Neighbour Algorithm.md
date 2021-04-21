# K-Nearest Neighbour Algorithm

KNN belongs to a group of lazy learners where as logistic, SVM, Neural Nets belong to Eager Learners. Lazy learners store the training data in memory and arranges the data in order to find the closest neighbours efficiently during the inference phase. Otherwise, it will have to compare every new case with whole dataset making it quite inefficient.

**Eager Learners :** During the training phase, the algorithm tries learn the best fit line that need a lot computations and take a lot of time.
**Lazy Learners :** They don't involve many computations and hence train much faster.

### How K-NN works ?
1.  Calculate the distance of K no of nearest neighbours.
2.  How many nearest belong to each category
3.  Finally, the classification is done based on maximum no of neighbours of the cteagories found.


Metrics such as Ecludian, Manahattan distance calculations are used to find the nearest neighbours.

In case of imbalanced dataset and outliers, the KNN can be biased w.r.t output.
