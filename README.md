# Concrete-Strength-Prediction-
Deep learning regression model to predict concrete compressive strength using Keras
README

Overview

This repository contains a project demonstrating the performance improvement of a neural network model on a concrete strength prediction dataset. The dataset used for this project is publicly available here.

The project explores how different configurations of the model impact its performance, evaluated using Mean Squared Error (MSE). Key configurations include data normalization, increasing training epochs, and adding hidden layers to the network.

Dataset

File Path: https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/DL0101EN/labs/data/concrete_data.csv

Description: The dataset contains various features related to concrete composition, including cement, water, aggregate, and superplasticizer, among others, with the target variable being the compressive strength of the concrete.

Experiments

Baseline Model

Configuration:

1 hidden layer with 10 nodes

ReLU activation function

Trained for 50 epochs

Results:

Mean MSE: 392.03

Standard Deviation of MSE: 380.52

Insights: The baseline model exhibits high MSE and variance, suggesting poor generalization, potentially due to unnormalized input data or insufficient training epochs.

Part A: Normalized Data

Configuration:

Normalized all input features

Same architecture as the baseline

Results:

Mean MSE: 305.72

Standard Deviation of MSE: 161.69

Insights: Normalizing data significantly improved performance by helping the optimizer converge efficiently. Both the mean and variance of the MSE decreased.

Part B: Increased Epochs (100 Epochs)

Configuration:

Normalized data

Same architecture as the baseline

Training epochs increased to 100

Results:

Mean MSE: 251.75

Standard Deviation of MSE: 13.03

Insights: Doubling the number of epochs improved performance further by allowing the model to learn more effectively. The variance decreased significantly, indicating stable predictions across different data splits.

Part C: Increased Hidden Layers (3 Layers)

Configuration:

Normalized data

3 hidden layers

Each layer with 10 nodes and ReLU activation

Trained for 100 epochs

Results:

Mean MSE: 220.36

Standard Deviation of MSE: 17.89

Insights: Adding hidden layers allowed the model to capture more complex relationships in the data, resulting in the best performance among all configurations. The variance remained low, ensuring stable results.

Comparative Insights

Normalization: Essential for gradient-based optimizers like Adam. Drastically improves performance and reduces variance.

Increased Epochs: Enables the model to converge to better solutions, reducing both the mean MSE and variance. However, overfitting risks must be monitored.

Deeper Networks: Provide the best performance but require careful tuning and regularization to prevent overfitting.

Recommendations

Normalize Data: Always normalize input features to optimize model performance.

Start Simple: Begin with simpler models (fewer layers and epochs) and gradually add complexity based on performance metrics.

Monitor Validation Metrics: Regularly monitor validation metrics during training to identify overfitting early.

Experimentation: Test different configurations and parameters to identify the optimal model for your use case.

How to Use This Repository

Download Dataset:
Download the dataset from the given URL and place it in your working directory.

Preprocess Data:
Ensure the dataset is normalized before training the model.

Train Models:
Experiment with different configurations (hidden layers, epochs, etc.) and observe the impact on performance metrics.

Evaluate:
Use MSE and its variance as the primary metrics to compare model performance.

Acknowledgments

IBM's Data Science Program: The dataset and inspiration for this project are from IBM's "Deep Learning and Neural Networks" course.

