# K-Means Clustering Algorithm

It's one of the unsupervised machine learnign algorithms that groups or classifies data points, based on several similarities in the data set which allows certain patterns to evolve upon which the prediction is done.

Clustering is to group similar objects that are highly dissimilar in nature. For a better understanding of clustering, we need to differentiate the concept of **Heterogeneity between the groups and Homogeneity within the groups.**  This can be broken down by understanding the variance in the data points between the groups and the variance within the groups. The variance between the groups (also referred to as clusters) is the distance between the points from one cluster to the other. In case, two clusters are being formed from a dataset, the statistical calculation of the variance between the clusters will adhere to the rule below:

  **Sum of Squares Between the Groups > Sum of Squares within the groups i.e -----> SSB> SSW**

##### For a better understanding of clustering, a graphical representation is shown below:

![image](https://user-images.githubusercontent.com/30498799/115366678-1d45b100-a1f8-11eb-9a80-3d1c2a29f1a6.png)

#### There are few methods for measuring the variance

1.  **Ecludian Distance:** _When the Euclidean distance between 2 clusters is small, it means the features between the clusters are similar in nature._
2.  **Manhattan Distance:** _It is an extension of Euclidean distance calculation and instead of taking squares of the data points we takle in ecludian distance, we take the modulus of the difference between data points, rather than squaring them._

<u> _Statistically, it can be depicted as_: </u>

For Eg: If we have 2 points (x1, y1) and (x2, y2) = (5,4) and (1,1)

Manhattan Distance= |5-1|+|4-1|= 7

In the case of Euclidean distance calculation:

Euclidean Distance = SQRT[(5-1)^2+(4-1)^2]=5

3.  **Chebyshev Distance:** _It considers the maximum value of all the distances based on the Manhattan method._


The **“Jaccard”** method of variance calculation can be used when the variable **data type is Boolean in nature**.

##### A full reference on different distance metrics that are available for calculation:

|Identifier|Class name|args|Distance Function|
|----|-----|-------|-------|
|"euclidean"|Euclidean Distance||sqrt(sum((x – y)^2))|
|"manhattan"|Manhattan Distance||sum(|x – y|)|
|"chebyshev"|Chebyshev Distance||max(|x – y|)|
|"minkowski"|Minkowski Distance|p|sum(|x – y|^p)^(1/p)|
|"wminkowski"|WMinkowski Distance|p, w|sum(|w * (x – y)|^p)^(1/p)|
|"seuclidean"|SEuclidean Distance|V|sqrt(sum((x – y)^2 / V))|
|"mahalanobis"|Mahalanobis Distance|V, VI|sqrt((x – y)’ V^-1 (x – y)|

