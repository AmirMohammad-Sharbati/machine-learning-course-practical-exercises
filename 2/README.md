# Explanation of Second Assignment


---
## K_Means:

### 1. load_image
- Uses PIL to load the image and convert it to RGB.
- Converts to a NumPy array.
- Normalizes pixel values to the range 0–1 for easier distance calculations.

### 2. preprocess_image
- Flattens image from (height, width, 3) to (num_pixels, 3).
- That's required because K-Means operates on a list of pixel vectors.

### 3. initialize_centers
- Selects k random pixels; these become the initial centroid colors.

### 4. assign_clusters
- Computes Euclidean distance from each pixel to each center.
- Assigns each pixel to the closest center.

### 5. update_centers
- For each cluster, computes the mean RGB value of its assigned pixels.
- Handles empty clusters by assigning a random pixel.

### 6. kmeans
Repeatedly:
- Assign pixels → clusters
- Recompute centers
- Stops when centers move less than a tolerance (tol) or max iterations reached.

### 7. Recreate_image
- centers[labels] maps each pixel label to its centroid color.
  (Example: if pixel belongs to cluster 2 → use centers[2])
- Then we reshape back from (num_pixels, 3) to (height, width, 3).
- This forms the final segmented image.

### 8. calculate_wcss and plot_elbow
For each K from 1 to max_k:
- Run K-Means
- Compute WCSS = sum of squared distances from each pixel to its cluster centroid
- Append to list
- Plots K vs WCSS
- The “elbow” drop indicates a good choice of K.

### 9. Run the segmentation
- Load the image and prepare normalized pixels for K-Means.
- Use raw (0–255) pixels for WCSS so values stay in the correct scale.
- Run K-Means to get cluster centers and labels for each pixel.
- Recreate the segmented image by replacing each pixel with its cluster center.
- Subsample raw pixels to compute WCSS faster.
- Calculate WCSS for different K values to use in the Elbow Method.

### 10. Display results
- Plot the original image and the segmented image side by side for comparison.
- Turn off axes for a cleaner visualization.
- Plot the Elbow Method graph to show how WCSS changes with K and help estimate the optimal number of clusters.



---
## GMM:

### 1. gaussian_pdf_all(X, mean, cov)
#### Theory
Computes the probability density of each data point under a multivariate Gaussian distribution:

N(x∣μ,Σ)=1(2π)d/2∣Σ∣1/2exp⁡(−12(x−μ)TΣ−1(x−μ))
N(x∣μ,Σ)=
(2π)
d/2
∣Σ∣
1/2
1
	​

exp(−
2
1
	​

(x−μ)
T
Σ
−1
(x−μ))

Where:
- X is shape (n_samples, n_features)
- Output is a vector of size (n_samples,)
Purpose
- GMM needs these densities to calculate responsibilities (soft cluster assignments).


### 2. initialize_parameters(X, k, rng)
Theory
- We randomly initialize:
- weights πₖ (sum to 1),
- means μₖ (random data points),
- covariances Σₖ (start with identity or sample covariance).
This gives a starting point for EM.
Purpose
- GMM is sensitive to initialization; this step makes EM start somewhere reasonable.


