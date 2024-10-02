# Country-Segmentation-Using-Unsupervised-Machine-Learning
## Introduction
This project focuses on applying clustering algorithms in machine learning, specifically the k-means and Mean-Shift models, to a dataset of countries characterized by various economic and social indicators. Unsupervised machine learning is employed to discover underlying patterns within the data, with clustering being a common approach for identifying groups in datasets that contain features and observations.

## K-means:
K-means is a centroid-based clustering algorithm that starts by selecting a predetermined number of clusters (k). It assigns each data point to these clusters based on their Euclidean distance. The algorithm iteratively updates the positions of the centroids by calculating the mean of all data points assigned to each cluster until an optimal arrangement is reached.

## Mean-Shift:
In contrast, Mean-Shift does not require a preset number of clusters. Instead, it allocates each data point to the peaks it identifies within the dataset, concentrating on finding areas of high density. This characteristic makes Mean-Shift particularly useful when the number of clusters is uncertain.

## Model Construction and Implementation
The data undergoes pre-processing and exploratory analysis to confirm its suitability. Significant features, including exports (ranging from 0 to 200) and imports (ranging from 0 to 174), show a strong positive correlation. Child mortality rates vary from 2 to 208. A basic k-means and Mean-Shift algorithm is applied, initially clustering based on child mortality and exports before incorporating additional features.

## Observations
The k-means model effectively divided the dataset into five clusters. Notably, Cluster 3 comprises countries with low child mortality and limited exports, indicating favorable healthcare and socio-economic conditions. Cluster 0 represents the most advantageous scenario, characterized by low child mortality and high exports. Cluster 2 includes countries with better child mortality rates and significant exports. Conversely, Cluster 4 reveals higher child mortality and poor export performance, while Cluster 1 contains countries that perform poorly in both metrics, with some outliers showing average export levels.

## Comparison of Mean-Shift and k-Means
The Mean-Shift and k-means clustering methods produce different results. K-means suggests around five optimal clusters, while Mean-Shift indicates a more effective three-cluster solution. In various analyses, k-means (with five clusters) provides deeper insights, with notable similarities between k-means Cluster 0 and Mean-Shift Cluster 1. Differences appear in features such as imports and exports, where k-means identifies three clusters, whereas Mean-Shift shows four. Further analysis with three features reveals varying optimal cluster counts (six for k-means and three for Mean-Shift) and distinct cluster assignments for certain data points.

## Evaluation and Recommendations
The elbow plot technique was initially utilized to determine the optimal number of clusters for k-means and was subsequently evaluated using silhouette scores for accuracy. Additional features from the dataset were integrated, and both k-means and Mean-Shift models were applied to extract further insights, proving advantageous. Throughout the algorithmic process, both models consistently identified a cluster with three or four data points, representing the best-performing countries based on economic and social indicators. Additional analysis using Python, which assigned these clusters to the complete dataset, highlighted these countries as Luxembourg, Switzerland, Qatar, and Singapore. Occasionally, Norway was also included as a fifth country.
