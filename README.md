# FashionMNISTdata
Comparison MLP vs CNN architectures
# 🧠 MLP vs CNN on Fashion MNIST

This project compares two different neural network architectures for image classification using the [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist) dataset:
- A NumPy-based **Multilayer Perceptron (MLP)**
- A TensorFlow/Keras-based **Convolutional Neural Network (CNN)**

---

## 📊 Dataset
Fashion MNIST is a dataset of 28x28 grayscale images of clothing items with 10 classes:
- T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot

Each image is labeled with the item class and the dataset is split into 60,000 training and 10,000 testing examples.

---

## 🏗️ Models Compared

### 🔷 1. MLP (from scratch using NumPy)
- **Architecture**: Input (784) → Hidden (512, ReLU) → Output (10, Softmax)
- **Optimizer**: Manual gradient descent
- **Loss**: Cross-entropy
- **Framework**: Pure NumPy

### 🔶 2. CNN (TensorFlow/Keras)
- **Architecture**: 
  - Conv2D → ReLU → MaxPooling
  - Conv2D → ReLU → MaxPooling
  - Flatten → Dense(128, ReLU) → Dropout(0.5) → Dense(10, Softmax)
- **Optimizer**: Adam
- **Loss**: Sparse Categorical Crossentropy
- **Framework**: Keras (TensorFlow)

---

## 📈 Results

| Model | Accuracy (Test) | Training Time | Remarks |
|-------|------------------|----------------|---------|
| MLP (NumPy) | ~85% | Slow (no GPU) | Good baseline |
| CNN (Keras) | ~92–94% | Fast (GPU-enabled) | Stronger feature extraction |

---
