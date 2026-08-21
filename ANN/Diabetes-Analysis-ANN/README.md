# Diabetes Analysis Using Artificial Neural Network (ANN)

## Overview
This project focuses on predicting diabetes using an Artificial Neural Network (ANN).  
The objective is to classify whether a patient has diabetes based on medical and demographic features.

---

## Data Preprocessing

- Removed irrelevant columns (e.g., `id`)
- Handled categorical features using one-hot encoding
- Ensured consistent feature alignment between training and test data
- Applied feature scaling using `StandardScaler`
- Used stratified train-test split to maintain class balance

---

## Model Architecture

The ANN model consists of:

- Input layer matching number of features
- Dense layer with ReLU activation
- Batch Normalization
- Dropout layers for regularization
- Additional Dense layers
- Output layer with Sigmoid activation (binary classification)

**Loss Function:** Binary Crossentropy  
**Optimizer:** Adam  

---

## Training Strategy

- Implemented Early Stopping to prevent overfitting
- Used Dropout for better generalization
- Tuned decision threshold using Precision-Recall analysis
- Evaluated model using:
  - Accuracy
  - Precision
  - Recall
  - F1-score

---

## Results

- Achieved balanced performance across both classes
- Improved recall for positive class through threshold tuning
- Reduced overfitting using regularization techniques
- Current accuracy is moderate and stable

---

## Future Improvements

- Hyperparameter tuning
- Learning rate adjustments
- Architecture optimization
- Feature engineering
- Advanced regularization techniques

---

## Conclusion

The ANN model demonstrates reasonable performance for diabetes prediction.  
Further refinements are being explored to enhance accuracy and generalization capability.