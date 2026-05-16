# MNIST Handwritten Digit Classification using PyTorch

This project implements a **Multi-Layer Perceptron (MLP)** neural network using **PyTorch** to classify handwritten digits from the MNIST dataset.

Two different experiments were conducted with different architectures and activation functions to compare performance.

---

# Project Overview

The project includes:

- Loading and preprocessing the MNIST dataset
- Building a customizable MLP model
- Training and validation loops
- Model evaluation on test data
- Comparing multiple experiments
- Visualizing loss and accuracy curves

---

# Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib

---

# Dataset

The project uses the **MNIST Handwritten Digits Dataset** provided by Torchvision.

- Training images: 60,000
- Test images: 10,000
- Image size: 28 × 28 grayscale

Dataset Link:  
(https://docs.pytorch.org/vision/stable/generated/torchvision.datasets.MNIST.html)

The dataset is automatically downloaded when running the code.

---

# Data Preprocessing

The following transformations are applied:

```python
transforms.Compose([
    transforms.ToTensor(),
    transforms.Normalize((0.5,), (0.5,))
])
```

### Preprocessing Steps

1. Convert images into tensors
2. Normalize pixel values for better training stability

---

# Model Architecture

The model is a simple fully connected neural network (MLP).

## Architecture

```text
Input Layer: 28×28 = 784 neurons
Hidden Layer 1
Activation Function
Hidden Layer 2
Activation Function
Output Layer: 10 neurons
```

---

# Experiments

## Experiment 1

| Parameter | Value |
|---|---|
| Hidden Layer 1 | 128 |
| Hidden Layer 2 | 64 |
| Activation Function | ReLU |
| Learning Rate | 0.001 |

### Results

- Test Accuracy: **96.60%**
- Test Loss: **0.1095**

---

## Experiment 2

| Parameter | Value |
|---|---|
| Hidden Layer 1 | 256 |
| Hidden Layer 2 | 128 |
| Activation Function | Tanh |
| Learning Rate | 0.0005 |

### Results

- Test Accuracy: **97.30%**
- Test Loss: **0.0855**

---

# Training Process

The training loop performs:

- Forward propagation
- Loss computation using CrossEntropyLoss
- Backpropagation
- Parameter updates using Adam optimizer

Validation is performed after every epoch.

---

# Evaluation

The model is evaluated on the MNIST test dataset using:

- Test Loss
- Test Accuracy

---

# Visualizations

The project generates:

1. Loss comparison plot
2. Accuracy comparison plot

These plots help compare training and validation performance across experiments.

---

# How to Run

## 1. Clone Repository

```bash
git clone https://github.com/Mokhalil101/Handwritten-Digit-Recognition-using-MLP-MNIST-.git
cd Handwritten-Digit-Recognition-using-MLP-MNIST-
```

---

## 2. Install Requirements

```bash
pip install -r requirements.txt
```

---

## 3. Run the Project

```bash
python main.py
```

---

# requirements.txt

```txt
torch
torchvision
matplotlib
numpy
```

---

# Project Structure

```text
├── data/
├── main.py
├── requirements.txt
├── README.md
```

---

# Results Summary

| Experiment | Test Accuracy |
|---|---|
| Experiment 1 | 96.60% |
| Experiment 2 | 97.30% |

Experiment 2 achieved the best performance.

---

# Future Improvements

Possible improvements for this project:

- Add Dropout layers
- Use Convolutional Neural Networks (CNNs)
- Hyperparameter tuning
- Add confusion matrix visualization
- Save and load trained models

---
