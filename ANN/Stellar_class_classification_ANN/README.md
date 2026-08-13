# 🌌 Stellar Classification using Artificial Neural Networks (ANN)

A deep learning project that uses an **Artificial Neural Network (ANN)** to classify stellar objects based on their astronomical characteristics.

This notebook was developed for the **Kaggle Playground Series (Season 6, Episode 6) Stellar Classification Competition**. The model is trained on tabular astronomical data and predicts the class of a celestial object using multiple physical and spectral features.

Because apparently even stars need to be sorted into categories. Humans looked at a galaxy containing billions of objects and collectively decided, "Let's make a spreadsheet."

---

## 📌 Project Overview

The workflow followed in this project includes:

1. Loading the training and testing datasets.
2. Exploring class distributions.
3. Encoding categorical features.
4. Standardizing the input data.
5. Building an ANN using TensorFlow and Keras.
6. Training the model to classify stellar objects into different categories.

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* TensorFlow
* Keras
* Kaggle Notebook Environment

---

## 📂 Dataset

Dataset source:

**Kaggle Playground Series - Season 6, Episode 6**

The dataset contains:

* Numerical astronomical features
* Spectral information
* Galaxy population data
* Stellar object classes

Files used:

* `train.csv`
* `test.csv`

---

## ⚙️ Data Preprocessing

### 1. Feature Encoding

Categorical features were converted into numerical values using **LabelEncoder**.

Encoded features:

* `spectral_type`
* `galaxy_population`
* `class` (training dataset only)

```python
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

traindata["spectral_type"] = le.fit_transform(
    traindata["spectral_type"]
)

traindata["galaxy_population"] = le.fit_transform(
    traindata["galaxy_population"]
)

traindata["class"] = le.fit_transform(
    traindata["class"]
)
```

---

### 2. Feature Scaling

The features were standardized using **StandardScaler**.

```python
from sklearn.preprocessing import StandardScaler

sc = StandardScaler()

x_train_scaled = sc.fit_transform(x_train)
```

Standardization ensures that all features contribute equally during training.

---

## 🧠 ANN Architecture

The neural network consists of:

| Layer          | Neurons            | Activation |
| -------------- | ------------------ | ---------- |
| Input          | Number of features | -          |
| Hidden Layer 1 | 128                | ReLU       |
| Hidden Layer 2 | 64                 | ReLU       |
| Hidden Layer 3 | 32                 | ReLU       |
| Output Layer   | 3                  | Softmax    |

Model definition:

```python
model = keras.Sequential([
    keras.layers.Input(shape=(x_train.shape[1],)),

    Dense(128, activation="relu"),
    Dense(64, activation="relu"),
    Dense(32, activation="relu"),
    Dense(3, activation="softmax")
])
```

---

## 📁 Project Structure

```text
stellar-classification-ann/
│
├── stellar-class-competition-ANN.ipynb
├── train.csv
├── test.csv
└── README.md
```

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
```

Install the required dependencies:

```bash
pip install numpy pandas scikit-learn tensorflow keras
```

---

## ▶️ Running the Project

Open the notebook:

```bash
jupyter notebook stellar-class-competition-ANN.ipynb
```

Run all cells sequentially to:

* Load the dataset
* Preprocess the data
* Train the ANN
* Generate predictions

---

## 📈 Future Improvements

* Hyperparameter tuning
* Cross-validation
* Dropout regularization
* Batch normalization
* Learning rate optimization
* Comparison with traditional machine learning models

---

## 🤝 Contributions

Contributions, suggestions, and improvements are always welcome.

---

## 📜 License

This project is intended for educational and research purposes.
