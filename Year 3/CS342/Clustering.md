(Part of [[Unsupervised Machine Learning]])

Clusters form in the data where:
- points within a cluster are "similar"
- points in distinct clusters are "dissimilar"

**Problem:** How should we define "similarity"? 
**Problem:** How do we form the clusters?
**Problem:** Can we do it efficiently?

## K-Means Clustering

Have two phases:
- **Assignment:** Assign points to clusters based on how far they are from the current means
- **Update:** Calculate the means from the current assignment

**Algorithm:** Start with random means and run many iterations of assignment and update. We stop when either:
- the means don't change anymore
- some maximum number of iterations reached





