<img width="812" alt="Screenshot 2025-02-20 at 19 48 21" src="https://github.com/user-attachments/assets/51a362e9-db99-46c0-aed1-013995c470b3" />


AI4EO - WEEK 4 ASSIGNMENT

This code classifies the echoes in leads and sea ice and produces an average echo shape as well as standard deviation for these two classes. 
It aligns and plots 100 echoes using a K means clustering model and then a gaussian mixture model for clustering. The alignment is not perfect, but roughly aligns the echoes so that an average value can be found. The peak values for these two clustering methods are then compared using a box and whisker plot.
The echo classification is then compared against the ESA official classification using a confusion matrix.

<img width="551" alt="Screenshot 2025-02-20 at 19 46 11" src="https://github.com/user-attachments/assets/a8238043-21f4-4816-84b9-41b215c0dab8" />

K-means Clustering Overview:
K-means clustering is an unsupervised learning algorithm that partitions data into k pre-defined clusters based on feature similarity. It works by initializing k centroids, assigning each data point to the nearest centroid, and iteratively updating the centroids until minimal movement occurs.

Why Use K-means?

No prior data structure needed: Ideal for exploratory analysis.
Simple & scalable: Easy to implement and handles large datasets efficiently.
Key Components:

Choosing k: The number of clusters is user-defined.
Centroid Initialization: Starting positions impact final results.
Assignment Step: Data points are linked to their closest centroid.
Update Step: Centroids are recalculated based on assigned points.
Iterative Process:
The assignment and update steps repeat until centroids stabilize, minimizing within-cluster variation. The algorithm converges to a solution, though it may be a local optimum.

<img width="549" alt="Screenshot 2025-02-20 at 19 44 58" src="https://github.com/user-attachments/assets/80046248-2bbe-4cd8-9e50-2dcb3c8c7eaf" />

Gaussian Mixture Models (GMM) Overview:
GMM is a probabilistic model that represents data as a mixture of multiple Gaussian distributions, each with its own mean and variance. It’s widely used for clustering and density estimation, capturing complex data distributions through simpler Gaussian components.

Why Use GMM for Clustering?

Soft clustering: Assigns probabilities of data points belonging to each cluster, allowing for overlapping clusters.
Flexibility in shape & size: Supports clusters with varying sizes and orientations, unlike K-means.
Key Components:

Number of Components: Defines how many Gaussian distributions to use.
Expectation-Maximization (EM) Algorithm: Iteratively fits the model to maximize data likelihood.
Covariance Type: Controls the shape and orientation of clusters (e.g., spherical or full).
The EM Algorithm in GMM:

Expectation Step (E-step): Computes the probability of each data point belonging to each Gaussian.
Maximization Step (M-step): Updates Gaussian parameters (mean, covariance, mixing coefficient) to best fit the data.
This process repeats until the model parameters stabilize, ensuring convergence.

<img width="713" alt="Screenshot 2025-02-20 at 19 49 32" src="https://github.com/user-attachments/assets/8b0ae5ed-c36c-422b-85c6-634c91ab0041" />


This project used google colab, github and google drive.

The process began by opening a Google Colab notebook and mounting Google Drive using from google.colab import drive and drive.mount('/content/drive'). After authentication, a project folder was created in Drive, and Colab’s directory was set to this folder using %cd. The GitHub repository was then cloned with !git clone https://github.com/username/repository.git, and work continued within the cloned directory. Colab automatically saved changes to Drive. To push updates to GitHub, credentials were set using !git config, followed by staging, committing, and pushing changes with !git add ., !git commit -m "message", and !git push origin main, using a GitHub token. The files were stored in Drive.
