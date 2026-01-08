# KNN_Implementation
📌 Project Overview

This project implements the K-Nearest Neighbors (KNN) classification algorithm from scratch using Python, without relying on high-level machine learning libraries for the core algorithm.
The goal is to understand how KNN works internally, how predictions are made using distance calculations, and how the choice of k affects model performance.
The dataset consists of two numerical features (Gene One, Gene Two) and a binary target variable (Cancer Present).

⚙️ How Error Rate Is Calculated

To evaluate the performance of the KNN classifier, I compute the error rate on the test dataset.

Step-by-step process:

The dataset is split into training and test sets.

For a given value of k, each test data point is classified using the KNN algorithm.

The predicted label is compared with the true label.

The number of correctly classified test samples is counted.

Accuracy is calculated as:

Accuracy=Number of Correct Predictions out of total test prediction

Accuracy Rate=Accuracy/no of test examples
	​
Error Rate is then computed as:

Error Rate=1-Accuracy Rate

This process ensures that model performance is evaluated only on unseen data, avoiding data leakage.

📈 Error Rate vs k-Value Analysis

To understand how the choice of k affects performance, the model is evaluated for multiple values of k.

Procedure:

Only odd values of k are used (to avoid ties in binary classification).

k ranges from 1 to 29.

For each k, the error rate is calculated using the method described above.

All error rates are stored and plotted against their corresponding k values.

Why this matters:

Small k values lead to a more complex model that is sensitive to noise (high variance).

Large k values produce smoother decision boundaries but may underfit the data (high bias).

Plotting Error Rate vs k helps identify an optimal k that balances this trade-off.

The resulting curve provides a visual way to select a suitable k rather than relying on a single arbitrary value.
