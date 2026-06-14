# MSCS_634_Lab_3

## Purpose

The goal of this lab was to compare K-Means and K-Medoids on the Wine dataset and to see how each algorithm grouped the samples after data standardization. Rather than focusing only on cluster assignments, I wanted to understand how the two methods behaved, how well the clusters were separated, and how closely they reflected the original wine classes.

## What I Observed

The first thing that stood out was how similar the Silhouette Scores were. K-Means achieved a score of 0.2849, while K-Medoids achieved 0.2676. This suggests that both methods were able to find some structure in the dataset, although K-Means produced slightly better cluster separation.

The larger difference appeared in the ARI results. K-Means achieved an ARI of 0.8975 compared to 0.7411 for K-Medoids. To me, this was the strongest indication that K-Means captured the underlying class structure more effectively. The cluster visualizations supported that conclusion because the K-Means groups appeared slightly more distinct and organized.

## What I Learned

One thing I learned from this lab is that clustering quality is not always obvious from a plot alone. The visualizations were helpful, but the evaluation metrics provided additional context that would have been difficult to assess by inspection alone. Looking at both the Silhouette Score and ARI made it easier to understand not only how separated the clusters were, but also how closely they matched the actual wine categories.

I also gained a better understanding of why preprocessing matters. The descriptive statistics showed that the features used were on very different scales, underscoring the importance of standardization before applying distance-based clustering algorithms.

## Challenges and Decisions

The main challenge was interpreting the clustering results. Unlike classification problems, there is no single accuracy metric that immediately indicates whether the clustering is good or bad. I had to look at the metrics, visualizations, and cluster assignments together before drawing conclusions.

One decision I made was to use PCA for visualization. Since the dataset contains 13 features, plotting the original data directly would not provide a clear comparison. Reducing the data to two dimensions made it easier to compare the K-Means and K-Medoids cluster structures side by side.

Overall, K-Means produced the stronger results in this experiment, but the lab also showed that different clustering methods can reveal slightly different views of the same dataset.
