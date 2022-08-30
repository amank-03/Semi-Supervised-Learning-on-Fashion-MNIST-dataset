# Semi-Supervised-Learning-on-Fashion-MNIST-dataset

## Introduction
Clustering is usually used for problems related to unsupervised learning but we will use it as a pre-processing tool for semi-supervised learning. If we only have a few labels, we could perform clustering and propagate the labels to all the instances (or to the closest instances decided by percentile) in the same cluster. This technique can greatly increase the number of labels available for a subsequent supervised learning algorithm, and thus improve its performance.

## Data Set
Fashion-MNIST is a dataset of Zalando's article images—consisting of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes. Fashion-MNIST was intended to serve as a direct drop-in replacement for the original MNIST dataset for benchmarking machine learning algorithms. It shares the same image size and structure of training and testing splits.


## Methodology

Here initially, we cluster the data set using K Means Clustering, in this problem K= 300. 
Then we find the centroid of each cluster and label the centroids manually and train the model using these 300 labelled data. 
Later we would progate the label of the cetroid to, at first entire data point and then to a nearest fraction of points in each cluster and
train the model again and compare its performances.

## Results

| Model  | Baseline Accuracy |
| ------------- | ------------- |
| Logistic Regression  | 84.10%  |
| Random 300 clusters  | 77.76%  |

### Semi-Supervised Learning with Clustering

| Cluster  |  Accuracy |
| ------------- | ------------- |
| 50  | 66.28%  |
| 100  | 70.46%  |
| 200  | 76.73%  |
| 300  | 76.22%  |

### Semi-Supervised Learning with Clustering and Propagating Centroid label to within cluster data points
| Cluster  |  Accuracy |
| ------------- | ------------- |
| 300 | 77.09%  |

### Propagating Centroid label to 75th percentile closest to the centroid
| Cluster  |  Accuracy |
| ------------- | ------------- |
| 300 | 77.05%  |


