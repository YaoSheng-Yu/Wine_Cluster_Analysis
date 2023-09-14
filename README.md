# Wine Clustering Analysis 🍷

**Objective:** Explore the underlying structure and natural groupings within a labeled wine dataset to uncover hidden patterns and validate the labels.

---

## Why Cluster on a Labeled Dataset? 

- **Uncover Structure:** Understand the inherent groupings present in the data.
- **Validate Labels:** Ascertain if the given labels actually correspond to these intrinsic clusters.
- **Discover Patterns:** Shed light on concealed trends within the data.

---

## Choosing Variables 

For this analysis, two pivotal variables were chosen:

1. **Color:** A prominent feature influencing consumers' wine preferences.
2. **Flavanoids:** Abundantly found in wines, affecting wine's bitterness, astringency, and complexity.

---

## K-means Clustering 💠

![K-means GIF](./iterations%20gif/kmeans_animation.gif)

### Methodology: 
- Start with random cluster centers, or 'centroids'.
- Calculate centroids based on feature means.
- Reassign data points to the nearest centroid.
- Recalculate centroids and repeat until clusters stabilize.
  
### Observations:
- Over iterations, distinct shifts in cluster boundaries and memberships are observed.
- Wine type primarily gets distinguished by color (y-axis), suggesting its importance.
- The **Adjusted Rand Index (ARI)** for this method is 0.45, indicating moderate cluster quality.

---

## EM Algorithm 🔄

![K-means GIF](./iterations%20gif/kmeans_animation.gif)

### Two-Step Process:
EM operates on the assumption that data is generated from a mixture of Gaussian distributions.
1. **E-step:** Assigns data point probabilities to each cluster based on current parameters.
2. **M-step:** Updates these parameters to maximize the likelihood of observing the given data.

### Observations:
- Both the x and y-axes (Flavanoids & Color) play a role in clustering.
- Achieved an **Adjusted Rand Index (ARI) of 0.754**, suggesting superior cluster quality as compared to K-means.
  
---

## K-means vs EM: Key Differences 🔍

- **Model Assumptions:** K-means assumes spherical clusters with the same variance, while EM employs Gaussian distributions for each cluster.
- **Assignment:** K-means uses 'hard' assignment, placing each data point in one cluster. In contrast, EM operates on 'soft' assignments based on probabilistic inferences.
- **Outliers:** K-means can be sensitive to outliers, while EM's probabilistic approach can handle them more gracefully.

---

## Conclusion & Reflections 🌟

This project showcased the ability to utilize clustering methodologies to analyze and understand inherent patterns in data. While labels are available, clustering provided insights into the validity of these labels and emphasized the different strengths and nuances of K-means and EM clustering techniques. 

---

**End Note:** For potential recruiters viewing this, this project serves as a testament to my data analytics prowess and my ability to extract meaningful patterns from complex data sets.

---

## Tools & Libraries 🛠️

- **R**
- **ggplot2** for visualizations
- **mclust** for EM clustering

---

## Further Exploration 🚀

- Test additional clustering methods.
- Incorporate more features from the wine dataset.
- Explore dimensionality reduction techniques to better visualize higher-dimensional data.


