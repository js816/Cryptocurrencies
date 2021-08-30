# Cryptocurrencies

# Overview of the Project

Martha, who works for Accountability Accounting, wants to make a pitch that her company should invest in cryptocurrency.  To help better understand the relationships between the various cryptocurrencies, Martha and I used unsupervised machine learning to cluster together the various cryptocurrencies.  


# Results

## Data preprocessing

Before unsupervised machine learning can be used, the data must be transformed to match the requirements of the algorithm and the project.  In our case, only cryptocurrencies that are being traded and that have coins that have been mined were included.  Currencies with any null values were removed.  Non-numeric features (the algorithm type and proof type) were converted to numeric columns to allow those features to be analyzed.  The data was then scaled to ensure the accuracy of our model.


## Feature reduction

After performing the above preprocessing, our data had 98 columns.  To enhance the efficiency of our model and provide easier visualization of the data, those features were reduced using Principal Component Analysis (PCA).  We reduced the data to 3 principal components (PC1, PC2, and PC3).


## Clustering

After reducing the number of columns in our dataset, the elbow curve was plotted to determine the optimal number of clusters.  

![Elbow_curve](https://user-images.githubusercontent.com/82730954/131226090-a1ac59a0-6f9a-4003-bd8e-37d048f0289f.PNG)

Based upon the curve, 4 clusters were chosen and the KMeans algorithm was used to predict the members of each cluster.

The image below shows the clustering of the cryptocurrency.  In the Jupyter Notebook file, each of the markers can be hovered over to see the currency name, cluster, algorithm, and each principal component value.

![Clusters](https://user-images.githubusercontent.com/82730954/131226097-4a3bd1b6-115f-4156-98da-371137c03406.png)

Additionally, a sortable and selectable table was created in the file that contains the details for each currency.

![Table](https://user-images.githubusercontent.com/82730954/131226105-a059a8da-6971-4967-8317-b964c5fef5db.PNG)


# Summary

With the clusters that have been created, Accountability Accounting can now look at each cluster together to analyze potentially investing in cryptocurrencies.  The clusters allow more meaningful and insightful conversations about grouped currencies instead of attempting to look at unrelated currencies together.

Additionally, now that we have a clean and clustered dataset, we could consider using supervised machine learning if there are particular datapoints we’re interested in predicting.
