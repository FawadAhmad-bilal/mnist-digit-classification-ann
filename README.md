# 🔢 Handwritten Digit Classification using ANN | MNIST Dataset

Classifying handwritten digits (0–9) from the famous MNIST dataset using a fully connected Artificial Neural Network built with Keras and TensorFlow.

---

## 📌 Problem Statement

Given a 28×28 grayscale image of a handwritten digit, predict which digit (0–9) it represents. This is a **multi-class classification problem** with 10 output classes.

---

## 📊 Dataset

- **Source:** `keras.datasets.mnist` (built-in)
- **Training Samples:** 60,000 images
- **Test Samples:** 10,000 images
- **Image Shape:** 28 × 28 pixels (grayscale)
- **Classes:** 10 (digits 0–9)

---

## 🧠 Model Architecture

```
Input       → Flatten(28×28) = 784 features
Hidden Layer 1 → 120 neurons, ReLU activation
Hidden Layer 2 → 30 neurons, ReLU activation
Output Layer → 10 neurons, Softmax activation
```

- **Loss Function:** Sparse Categorical Crossentropy
- **Optimizer:** Adam
- **Epochs:** 14
- **Validation Split:** 20%

---

## ⚙️ Workflow

```
Load MNIST → Normalize (÷255) → Build ANN
→ Train → Predict Probabilities → argmax → Evaluate
```

1. Load dataset using `keras.datasets.mnist`
2. Normalize pixel values to [0, 1] by dividing by 255
3. Build Sequential ANN with Flatten + Dense layers
4. Train for 14 epochs with validation
5. Predict class probabilities using `model.predict()`
6. Get final class using `argmax(axis=1)`
7. Evaluate using **Accuracy Score**

---

## 📈 Results

| Metric | Value |
|---|---|
| Test Accuracy | ~97%+ |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-Sequential-red)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-metrics-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-visualization-purple)

---

## 🖼️ Sample Prediction

```python
# Predict a single image
model.predict(x_test[7].reshape(1, 28, 28)).argmax(axis=1)
```

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/FawadAhmad-bilal/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install tensorflow scikit-learn numpy matplotlib

# Run the notebook
jupyter notebook mnist_classification.ipynb
```

> Dataset downloads automatically via `keras.datasets.mnist.load_data()`

---

## 📁 Project Structure

```
├── mnist_classification.ipynb
└── README.md
```

---

## 🔗 Related Projects

- [Graduate Admission Prediction using ANN](../graduate_admission/)
- [Customer Churn Prediction using ANN](../customer_churn/)

---

## 👤 Author

**Fawad Ahmad**  
BS Artificial Intelligence — University of Haripur  
[GitHub](https://github.com/FawadAhmad-bilal)
