This project was submitted for the **Quantum AI Hackathon** by Team 3.
--------------------------------------
Team Members
--------------------------------------

| Name              | Role in Project    |
| ----------------- | ------------------ |
| Abdelrahman Hafez | Data Preprocessing |
| Omar Youssef      | Model Development  |

--------------------------------------
## Project Overview

We tackled the challenge of predicting key weather metrics—temperature, precipitation, and wind speed—using a hybrid AI approach. Team 3 combined **classical machine learning** with **quantum neural networks (QNNs)** to leverage the strengths of both techniques. Classical models, such as Random Forests, helped identify the most relevant features, which were then used to train quantum models using Qiskit’s `EstimatorQNN`. This approach enabled us to evaluate quantum AI’s potential in real-world regression tasks, supported by classical preprocessing.

## Step by Step Explanation

#### 1. Data Preprocessing
- Cleaned the dataset: removed empty visibility columns and irrelevant snowfall data
- Dropped redundant min/max features, keeping only mean values
- Scaled features to −1,1 for model training

#### 2. Classical Modeling (Feature Selection)
- Used Random Forest Regressors to:
- Identify the top 5 most important features for each target variable
- Provide a baseline prediction for temperature, precipitation, and wind speed

#### 3. Quantum Model Development
- Built separate Quantum Neural Network (QNN) models for each target
- Implemented using Qiskit EstimatorQNN with ZZFeatureMap for feature encoding
- Optimized with SPSA and monitored convergence with callback logging

#### 4. Model Evaluation
- Assessed quantum models using R² scores on train and test sets
- Visualized true vs. predicted performance for each target
- Achieved moderate predictive performance (R² ≈ 0.3), highlighting potential for future quantum enhancements