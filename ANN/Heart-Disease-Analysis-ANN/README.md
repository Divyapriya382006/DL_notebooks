# Heart Disease Prediction using Artificial Neural Network

## Overview
This project implements an Artificial Neural Network (ANN) to predict the probability of heart disease based on patient health indicators. The model performs binary classification and was developed for a Kaggle competition focused on beginner-friendly machine learning workflows.

## Model Description
- Model Type: Artificial Neural Network (ANN)
- Architecture:
  - Input layer matching the number of features
  - One hidden dense layer with ReLU activation
  - Output layer with Sigmoid activation
- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Metric: Accuracy

## Features Used
- Age
- Sex
- Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Maximum Heart Rate
- Exercise-Induced Angina
- ST Depression
- Chest Pain Type (One-Hot Encoded)
- EKG Results (One-Hot Encoded)
- Slope of ST (One-Hot Encoded)
- Number of Vessels (Fluoroscopy)
- Thallium Test Results

## Data Preprocessing
- One-hot encoding for categorical features
- MinMax scaling for numerical features
- Binary thresholding where applicable
- Target variable separated before scaling

## Training
- Train-test split applied
- Model trained using Adam optimizer
- Achieved approximately 88% accuracy with balanced precision and recall

## Evaluation
- Accuracy score
- Precision, Recall, and F1-score
- Confusion Matrix visualization

## Submission Format
The submission file follows Kaggle’s required format:
id,Heart Disease 630000,0.23 630001,0.67 630002,0.11

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Seaborn

## Conclusion
This project demonstrates the application of an ANN for medical risk prediction, emphasizing proper preprocessing, model design, and evaluation. Performance can be further improved through hyperparameter tuning, deeper architectures, and regularization techniques.