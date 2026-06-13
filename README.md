# MSCS_634_Lab_3

## Purpose

This lab compares K-Means and K-Medoids clustering using the Wine dataset from sklearn. The main goal was not just to create clusters, but to see how well each method grouped the wine samples after the features were standardized. Since both algorithms depend on distance, scaling the data was an important step because features with larger numeric ranges could otherwise pull the clusters in a misleading direction.

## Key Insights

K-Means performed better than K-Medoids in this lab. K-Means produced a Silhouette Score of 0.2849 and an Adjusted Rand Index of 0.8975, while K-Medoids produced a Silhouette Score of 0.2676 and an Adjusted Rand Index of 0.7411.

The Silhouette Scores were close, which means both methods found some separation in the data. The bigger difference was in the ARI. K-Means matched the original wine classes much more closely, which suggests that its cluster assignments captured the structure of this dataset more effectively.

The visual comparison also supported this result. Both methods found similar groupings, but the K-Means clusters looked slightly cleaner and more organized. For this dataset, K-Means was the stronger method because the data appeared to respond well to centroid-based clustering.

## Challenges and Decisions

One challenge was interpreting the results because clustering does not work the same way as classification. There is no simple accuracy score during training because the model is not using the class labels to form clusters. To make the evaluation more meaningful, I used both the Silhouette Score and ARI. The Silhouette Score helped show how separated the clusters were, while ARI helped compare the cluster assignments with the actual wine classes.

Another decision was to use PCA for visualization. The Wine dataset has 13 features, so plotting the original feature space directly would not be practical. Reducing the data to two components made it easier to compare the K-Means and K-Medoids cluster patterns side by side.

Overall, this lab showed that K-Means was more effective for this dataset, while K-Medoids may still be useful in situations where outliers or unusual observations have a stronger effect on clustering behavior.
