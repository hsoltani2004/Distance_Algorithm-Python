

1. Euclidean distance

In mathematics, the Euclidean distance between two points in Euclidean space is the length of a line segment between the two points. It is the most commonly used algorism because it is simple and intuitive. Most situations can apply Euclidean distance. The formula is:


Python code:
```
from scipy.spatial import distance
distance.euclidean(vector_1, vector_2)
````

There are 2 disadvantages of Euclidean distance: it can not be applied to the data which is more than 3 dimensions; the data needs to be standardized before applying Euclidean distance.

2. Manhattan distance

Manhattan distance, also called taxicab geometry or city block, is a geometry whose usual distance function or metric of Euclidean geometry is replaced by a new metric in which the distance between two points is the sum of the absolute differences of their Cartesian coordinates.

It is usually used for discrete and binary data. The formula is:


Python code:
```
from scipy.spatial import distance
distance.cityblock(vector_1, vector_2)
```

3. Chebyshev distance


In mathematics, Chebyshev distance (or Tchebychev distance), maximum metric, or L∞ metric is a metric defined on a vector space where the distance between two vectors is the greatest of their differences along any coordinate dimension.

It is usually used for supply chain and logistics. The formula is:


Python code:
```
from scipy.spatial import distance
distance.chebyshev(vector_1, vector_2)
```

4. Minkowski distance


The Minkowski distance or Minkowski metric is a metric in a normed vector space which can be considered as a generalization of both the Euclidean distance and the Manhattan distance. It is more flexible than both of the distances. It depends on the p value to adjust the final result.

The formula is:


Python code:
```
from scipy.spatial import distance
distance.minkowski(vector_1, vector_2, p)
```
The disadvantage of Minkowski distance is we may need to calculate multiple times to find the best p value.

5. Cosine similarity


Cosine similarity measures the similarity between two vectors of an inner product space. It is measured by the cosine of the angle between two vectors and determines whether two vectors are pointing in roughly the same direction. It is often used to measure document similarity in text analysis.

The formula is:


Python code:
```
from scipy.spatial import distance
distance.cosine(vector_1, vector_2)
```

6. Haversine distance


The Haversine (or great circle) distance is the angular distance between two points on the surface of a sphere. It is usually used for navigation.

Formula:


Python code:
```
from sklearn.metrics.pairwise import haversine_distances
haversine_distances([vector_1, vector_2])
```

7. Hamming distance


Hamming distance is a metric for comparing two binary data strings. While comparing two binary strings of equal length, Hamming distance is the number of bit positions in which the two bits are different.

Example:


Python code:
```
from scipy.spatial import distance
distance.hamming(vector_1, vector_2)
```

The disadvantage of Hamming distance is it can only measure the distance of 2 vectors which have the same length.

8. Jaccard Index

The Jaccard Index is a metric that is used to determine how similar sample sets are. The length of the overlap dividing it by the total of the union of the sample sets is a formal definition of the measurement, which stresses resemblance between finite sample sets. It usually used for deep learning like images identify.

Python code:
```
from scipy.spatial import distance
distance.jaccard(vector_1, vector_2)
```

9. Sorensen-Dice coefficient


The Sørensen–Dice coefficient is a statistic used to gauge the similarity of two samples. It is usually used for text analysis.

Formula:


Python code:
```
from scipy.spatial import distance
distance.dice(vector_1, vector_2)
```

10. Dynamic Time Warping


Dynamic Time Warping (DTW) is a way to compare two -usually temporal- sequences that do not sync up perfectly. It is a method to calculate the optimal matching between two sequences. DTW is useful in many domains such as speech recognition, data mining, financial markets, etc.

Python code:
```
from scipy.spatial.distance import euclidean
from fastdtw import fastdtw
 
distance, path = fastdtw(timeseries_1, timeseries_2, dist=euclidean)
```
