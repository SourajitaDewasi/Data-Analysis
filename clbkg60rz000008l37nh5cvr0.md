# Introduction To Clustering

### INTRODUCTION TO CLUSTERING

Clustering is the process of forming clusters or groups of data points, but that is what Classification does too. So what is the magic? What Classification does is on labelled data, and what Clustering does is on unlabelled data. Unlabelled data is what the world is made of. A terrifying amount of unlabelled data that, if a machine is trained, could find brilliant underlying patterns.

### HOW IS CLUSTERING DIFFERENT FROM CLASSIFICATION?

**Clustering** divides the population or data points into several groups such that the data points in the same group are more similar than other data points. It creates a new feature which is the label in comparison to supervised learning techniques. It is an **Unsupervised Learning Technique**. Compared to **Classification**, where no physical data split is done, the characteristic of the data is changed. In Clustering, the physical division of the data is data with no feature of data being changed!

### HOW DOES CLUSTERING WORK ON UNLABELLED EXAMPLES?

***Step 1:*** Take Unlabelled Examples.

***Step 2:*** Define **Similarity Metric** based on similar features. Similarity Metric measures similarity between examples by combining the examples' feature data into a metric. With an increase in the number of features, the complexity of the similarity metric measure also increases.

***Step 3:*** Cluster them into similar groups and assign **Cluster ID**, condensing the entire feature set for an example into its Cluster ID or simply a number. It not only simplifies the entire feature data but also saves storage. Further Machine Learning Techniques can use this Cluster ID as a target label.

### TYPES OF CLUSTERING

There are four popular types of Clustering:

1.  *Centroid-based Clustering: Organizes data into non-hierarchial clusters and is very sensitive to initial conditions and outliers.* ***K-Means*** *is the most popular centroid-based clustering technique.*
    
2.  *Density-based Clustering: This clustering algorithm connects areas of high example density into clusters. It allows for arbitrarily shaped distributions as long as dense areas can be connected. It is disadvantaged for data of varying density and high dimensions.*
    
3.  *Distribution-based Clustering: This clustering method assumes data is composed of distributions such as Gaussian Distributions. This method is disadvantaged when the data distribution type is unknown; with the reduced probability of belonging to a distribution, the distance from the distribution's centre increases.*
    
4.  *Hierarchial-based Clustering: It creates a tree of clusters and is well-suited to taxonomical or hierarchical data.* By pruning the tree at the proper level, one can select any number of clusters. 
    

### EXAMPLES AND ADVANTAGES OF CLUSTERING

Clustering is used for social network analysis, search result grouping, market imaging, image segmentation, market segmentation anomaly detection and much more.

For example, We have seen SpotifyWrapped on our Spotify account. It is an example of data being collected and clustered. The feature data of a Spotify song includes the listener's data on location, time, type of song etc. The songs are included in playlists with timestamps, texts and user IDs. Clustering songs lets one replace all the sets of features using a single cluster-ID, thus reducing the data dimensions and also helping to preserve privacy in case many users are taken for Clustering.

### CONCLUSION

Clustering is an objective function. Any two points within a cluster show a similarity between the two in that sample. It is an unsupervised learning technique that helps us reduce data into cluster IDs and labels and find patterns in an unlabelled dataset.

Thanks for reading! ❤️

If you are studying the same course, let me know in the comments. Also, connect with me on my social: [LinkedIn](https://www.linkedin.com/in/sourajita-dewasi-52b3b4193/), [Twitter](https://twitter.com/SourajitaD) or [Github](https://github.com/SourajitaDewasi)!

**REFERENCES:**

1.  Correlated features and classification accuracy - Stack Overflow. [https://stackoverflow.com/questions/14813884/correlated-features-and-classification-accuracy](https://stackoverflow.com/questions/14813884/correlated-features-and-classification-accuracy)
    
2.  K-Means - TowardsMachineLearning. [https://towardsmachinelearning.org/k-means/](https://towardsmachinelearning.org/k-means/)