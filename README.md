# K-Means Clustering for Minute Weather Data Analysis

This project demonstrates how to perform K-means clustering on minute-granularity weather data using scikit-learn in Python. The goal is to generate a big-picture model of the weather patterns at a local station by grouping similar data points into clusters.

## Project Overview

This project involves the following steps:

1. **Data Loading and Sampling:** 
    - Load the weather data from a CSV file.
    - Sample the data to reduce computation time while maintaining representativeness.
2. **Data Cleaning:**
    - Handle missing values by dropping rows with empty `rain_accumulation` and `rain_duration` columns.
    - Identify and potentially address other data quality issues (optional).
3. **Feature Selection:**
    - Choose relevant features (columns) for clustering, such as air pressure, temperature, wind direction/speed, and relative humidity.
4. **Data Preprocessing:**
    - Standardize the features using `StandardScaler` from scikit-learn to ensure all features are on the same scale.
5. **K-Means Clustering:**
    - Apply K-means clustering with `n_clusters` set to 12 to create 12 clusters representing different weather patterns.
    - Analyze the cluster centers to understand the characteristics of each cluster.
6. **Visualization:**
    - Define functions to create Pandas DataFrames with cluster numbers and generate parallel coordinate plots to visualize the clusters based on selected features.
    - Create parallel coordinate plots for specific weather conditions (e.g., dry days, warm days, cool days).

## Usage

This project requires Python libraries like pandas, scikit-learn, and matplotlib. 

1. Ensure you have the required libraries installed.
2. Replace `"data/weather.zip"` with the path to your weather data file. 
3. Run the Python script.

## Output

The script generates output including:

- Sample data shape after sampling.
- Descriptive statistics of the sampled data.
- Number of rows dropped due to missing values.
- Selected features for clustering.
- K-means model object.
- Cluster centers representing the centroids of each cluster.
- Parallel coordinate plots visualizing the distribution of data points within clusters and for specific weather conditions.

## Further Exploration

- Experiment with different numbers of clusters (`n_clusters`) to see how it affects the results.
- Try other clustering algorithms and compare the outcomes.
- Incorporate additional features or weather data sources for a more comprehensive analysis.
- Explore dimensionality reduction techniques before clustering for high-dimensional datasets.

This project provides a basic framework for analyzing weather data using K-means clustering. You can customize and extend it to gain deeper insights into your specific weather dataset.
