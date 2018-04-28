# STA663-Final-Project: Scalable K-Means

### Team Members: Yunlu Hao, Lianghui Li

Include:   
  Kmeans.ipynb:   main file   
  data:           include all data files   
  test:           intermediate code   
  readme.md  

Package: 
  package_kmeans
  
  

This is the final project for course STA663. In this project, we implement the `K-means++` and `K-means||`algorithm in Python following Bahmani's paper "Scalable k-means++" and speed up using `Cython`,`JIT` and `multi-core processing`. 

We apply it to the simulated `GAUSSMIXTURE` dataset, `SPAM` and `Housing` dataset from UC Irvine Machine Learning repository. In this part, we compare clustering cost and runtime of the `k-means||` algorithm with these of random initialization and the `k-means++`. 

From the implementation on the simulated dataset and the real-world dataset, the `k-means||` and `k-means++` find a better initial centroids than random in most cases, which leads to a better final clustering performance. However, for our algorithm, `k-means++` runs faster than `k-means||` in most cases, in future anlysis, we should focus more on how to implement `k-means||` in a more robust setting(in terms of cost reduction and better parallel application.

We also created an easily instable package for our functions, which can be found in https://github.com/yumegaaru/package_kmeans

To install, please go to Terminal and type in:

```bash
!pip install --upgrade pip git+git://github.com/yumegaaru/kmeans_package.git
```

then run the following code in your python:

```python
import kemeans_package
```

Data and test code used in our analysis are also provided in folders under this repository.
