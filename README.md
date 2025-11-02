DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

This project implements the DBSCAN (Density-Based Spatial Clustering of Applications with Noise) algorithm in C.
DBSCAN is an unsupervised clustering method that groups together points that are closely packed while marking points in low-density regions as outliers.

DBSCAN/
│
├── circular_ring_dataset.c   # Generates a sample circular ring dataset for testing
├── dbscan.c                  # Main implementation of the DBSCAN algorithm
├── queue.c                   # Helper queue implementation for neighbor management
├── dbscan.png                # Example visualization of clustering results
├── readme.txt                # Basic project notes
└── README.md                 # Detailed documentation (this file)



Algorithm Overview

DBSCAN groups data points based on two parameters:

ε (eps): The maximum distance between two points to be considered neighbors.

MinPts: The minimum number of neighboring points required to form a dense region.

Steps:

For each unvisited point:

Find all neighbors within ε.

If the number of neighbors ≥ MinPts, start a new cluster.

Expand the cluster by recursively including all density-reachable points.

Points that do not belong to any cluster are labeled as noise.
