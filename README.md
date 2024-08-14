## Overview
This project explores the prediction of song success on Spotify using machine learning models. Specifically, we aimed to classify songs as 'Hits' or 'Flops' and to predict their stream counts. The project involves detailed data analysis, feature engineering, and the application of various machine learning algorithms to achieve these predictions.

## Problem Statement
In the music industry, the ability to predict a song's success can significantly influence marketing strategies and resource allocation. This project addresses the following key questions:

Classification: Can we accurately classify songs as 'Hits' or 'Flops' based on their audio features and metadata?
Regression: Can we predict the number of streams a song will receive?
These predictions provide actionable insights for artists, record labels, and streaming platforms, aiding in data-driven decision-making.

## Dataset
The dataset used is the "Most Streamed Spotify Songs 2023," consisting of 953 songs. The dataset includes various features:

Audio Attributes: Tempo (BPM), Key, Energy, Danceability, etc.
Chart Information: Presence on Spotify, Apple Music, Deezer, and Shazam charts.
Streaming Data: Total number of streams.
## Methodology
Data Preparation
Missing Data: Rows with missing values were removed to ensure the integrity of the analysis.
Standardization: Continuous variables were standardized to enhance model performance.
Feature Selection: Correlation analysis was conducted to identify and manage multicollinearity among predictors.
Models Applied
Logistic Regression:
AUC: Achieved an average AUC of 0.85 across 15 iterations for the classification task.
K-Nearest Neighbors (KNN):
Accuracy: The best-performing KNN model had an accuracy of 76% with an optimal K value of 10.
Random Forest:
MSE: For stream count prediction, the Random Forest model achieved the lowest MSE of 0.023.
AUC: In classification, Random Forest consistently achieved the highest AUC of 0.92.
Support Vector Machine (SVM):
Accuracy: SVM achieved a classification accuracy of 81%, with a corresponding AUC of 0.88.
MSE: For stream prediction, the SVM model recorded an MSE of 0.035.
Performance Metrics
Mean Squared Error (MSE): Used to evaluate the accuracy of regression models predicting stream counts.
Area Under the Curve (AUC): Used to assess the classification models' ability to distinguish between 'Hits' and 'Flops.'
## Results
Random Forest: Outperformed other models, achieving the highest AUC of 0.92 for the classification task and the lowest MSE of 0.023 for stream count prediction.
SVM: Showed strong performance with an AUC of 0.88 and an MSE of 0.035, though less consistent than Random Forest across different iterations.
Logistic Regression: While stable, it had a lower AUC compared to more complex models, averaging around 0.85.
KNN: Provided reasonable results but with lower predictive power, evidenced by an accuracy of 76%.
## Conclusion
The Random Forest model emerged as the most effective for both predicting whether a song would be a 'Hit' or 'Flop' and for estimating stream counts. However, the model's complexity suggests potential areas for future improvement, including model interpretability and computational efficiency.
