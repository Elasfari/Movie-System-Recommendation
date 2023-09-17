# Hybrid Recommender

This repository contains a hybrid recommender system that combines content-based and collaborative filtering techniques to provide movie recommendations. 

## Getting Started

To use this recommender system, you'll need to follow these steps:

1. Mount your Google Drive to access the necessary data files.
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

2. Install the required libraries.
   ```python
   !pip install surprise
   ```

3. Import the necessary libraries and load the data.
   ```python
   import pandas as pd
   import numpy as np
   from surprise import Reader, Dataset, SVD
   from surprise.model_selection import cross_validate
   from surprise.model_selection import KFold
   from sklearn.cluster import KMeans
   import matplotlib.pyplot as plt

   # Load the movie ratings data
   ratings = pd.read_csv('/content/drive/MyDrive/Data/ratings_small.csv')

   # Load other data files as needed (e.g., movies metadata)
   ```

4. Run the clustering analysis on ratings data to group ratings based on their values.
   ```python
   # Perform K-means clustering to divide ratings into clusters
   # Add cluster labels to the ratings dataframe
   # Check if the sample is good or not based on the cluster labels
   # Plot the elbow curve to determine the optimal number of clusters
   ```

5. Create a Surprise dataset and perform collaborative filtering.
   ```python
   # Create a Surprise dataset from the ratings data
   # Initialize the SVD algorithm and perform cross-validation
   # Train the SVD model on the entire dataset
   ```

6. Define a function for the hybrid recommender that takes user ID and movie title as input and returns movie recommendations.
   ```python
   def hybrid(userId, title):
       # Implement the hybrid recommender logic here
       pass
   ```

7. Use the `hybrid` function to get movie recommendations for a user and a movie title.

8. Enjoy personalized movie recommendations!

## Features

- Combines content-based and collaborative filtering techniques.
- Provides movie recommendations based on user preferences and movie similarity.
- Supports clustering analysis to group ratings and improve recommendations.
