# Predicting-and-Analyzing-Crop-Health-with-Remote-Sensing-Data-and-PyTorch

##Overview

This project leverages remote sensing data to analyze and predict vegetation health. Using raster and vector data, it calculates vegetation indices, such as the Normalized Difference Vegetation Index (NDVI), and classifies plots based on their health status. A machine learning model, specifically a neural network built with PyTorch, is employed for classification, with performance evaluation scores:-Accuracy Score: 0.95 &amp; Recall Score:0.9

## Highlights

- Data Processing: Handles raster data, including Digital Elevation Models (DEMs), orthophotos, and Digital Terrain Models (DTMs).

- Vegetation Indices: Computes NDVI to assess vegetation conditions.

- Data Filtering: Masks invalid data for elevation and thermal attributes.

- Zonal Statistics: Extracts mean NDVI, thermal, elevation, and DTM values for specific regions.

- Neural Network Model: Implements a PyTorch-based neural network for vegetation health classification.

- Performance Metrics: Assesses the model using accuracy, precision, recall, F1 score, and ROC-AUC.

## Data Sources

The dataset for this project can be obtained from publicly available remote sensing repositories or drone-based crop analysis platforms.

I have used this github repo to get data [https://github.com/dronemapper-io/CropAnalysis] which you can get from my data folder mentioned in this same repo.
and the remaining GeoTIFF data from the following url: [https://dronemapper.com/software/DroneMapper_CropAnalysis_Data.zip]

**Ensure that the both data is extracted into a data/ directory within your project structure.**

## Workflow

- Step 1: Load and Preprocess Data
  Load DEM, orthophoto, and DTM files using libraries such as rasterio.
  Filter out invalid values in elevation and thermal datasets.
  Calculate NDVI for vegetation analysis.

- Step 2: Zonal Statistics Computation
  Use the compute_zonal_stats() function to calculate mean NDVI, thermal, elevation, and DTM values for each plot in vector data.

- Step 3: Prepare Data for Modeling
  Create a feature matrix with NDVI and other zonal statistics.
  Generate synthetic labels to simulate vegetation health conditions.
  Address class imbalance using undersampling techniques.

- Step 4: Train the Neural Network
  Split the dataset into training and testing subsets.
  Standardize feature data for optimal model performance.
  Define and train a neural network model using PyTorch.

- Step 5: Evaluate Model Performance
  Evaluate the model using metrics such as accuracy, precision, recall, F1 score, and ROC-AUC.

## Results

The trained model demonstrates robust classification performance, achieving high accuracy and precision in identifying vegetation health status. Detailed results, including confusion matrix and metric scores, are available in the report.

## Future Directions

Explore additional vegetation indices and data sources.
Refine the neural network architecture for improved accuracy.
Extend the application to various crops and geographic regions.

## License
This project is licensed under the MIT License. Feel free to use and modify it as needed.
