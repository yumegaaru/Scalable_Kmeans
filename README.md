# STA663-Final-Project: Scalable K-Means

### Team Members: Yunlu Hao, Lianghui Li

This is the final project for course STA663. In this project, we implement the `K-means||` algorithm in Python following Bahmani's paper "Scalable k-means++" and speed up using `Cython` and `JIT`. 

We apply it to the simulated `GAUSSMIXTURE` dataset, `SPAM` and `Housing` dataset from UC Irvine Machine Learning repository. In this part, we compare clustering cost and runtime of the `k-means||` algorithm with these of random initialization and the `k-means++`. 

From the implementation on the simulated dataset and the real-world dataset, the `k-means||` and `k-means++` find a better initial centroids than random in most cases, which leads to a better final clustering performance. However, `k-means++` runs faster than `k-means||`, in future anlysis, we should focus on how to implement `k-means||` in parallel setting.
