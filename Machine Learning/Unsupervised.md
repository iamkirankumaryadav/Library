# Unsupervised Machine Learning Techniques

- Find Meaningful Structures and Patterns in the Observations
- Extract Important Features and Explore the Data Set in Detail.

### Clustering : 

- Automatically **Split** the Data Set into Groups According to Similarity. Good for Segmentation
- e.g. Determining Customer Segments in Marketing Data (Features : Gender, Location, Age, Education and Income)

### K Mean Clustering

- Cluster Data Points with Similar Characteristics 
- Iterative Process, Cluster changes every time according to the First Random Centroids of Cluster. 
- Different Starting Points create Different Clusters.
- **Elbow Method** : Sum of Squared Distance get smaller as the Number of Clusters Increases

Steps
1. Define Number of **Clusters** ( K )
2. Set Cluster Centre ( **Centroid** ) Randomly
3. Assign Points to Cluster
4. Calculate Centre ( **Centroid** ) of Each Cluster
5. Assign **Data Points** to New Clusters

### Hierarchical Clustering 

### A. Agglomerative

- Bootom Up Approach
- **AGNES** ( Agglomerative Nesting )
- Each **Data Point** is considered as an **Individual Cluster**
- At each Iteration, Similar Clusters merge with other **Clusters** until One Single Cluster remains. 

### B. Divisive

- Top Down Approach
- **DIANA** ( Divise Analysis )
- Dividing the **Single** Cluster into n **Clusters**

### How we Calculate Similarity between the Clusters
1. **MIN** ( Distance between the **Closest** Points of Two Clusters )
2. **MAX** ( Distance between the **Farthest** Points of Two Clusters )
3. Group **AVG** ( Average of Distance between Each Data Points of Two Clusters )
4. Distance between **Centroids** ( Distance between the **Centroid** of Two Clusters ) 

### Anomaly Detection : 

- Automatically Discover Unusual Data Points in Data Set.
- Used to Find Fraudulent Transactions, Identify an Outlier caused by Human Error during Data Entry.
- Reduces Complexity of Data and Helps to Understand Data more Clearly and Better Way.

### Feature Selection :

- Understanding Each Feature before using it for Machine Learning.
- Sometimes Irrelevant Features Affects the Accuracy of Correct Model.
- Selecting Important Features helps to Improve Accuracy, Not Every Feature Adds Value to Solve Problem.


### Association Mining :

- Set of Items that Frequently Occur together in Data Set.
- Basket Analysis : Items Bought Together | Goods Purchased at the Same Time Help to Develop Marketing Strategies.

### Dimensionality Reduction :
- Reducing the Number of Features (Irrelevant)

