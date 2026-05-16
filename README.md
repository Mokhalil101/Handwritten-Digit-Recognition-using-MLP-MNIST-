# 🧠 Handwritten Digit Recognition using Multilayer Perceptron (MLP)

# 📌 Overview

This project implements a **Handwritten Digit Recognition system** using a **Multilayer Perceptron (MLP)** neural network built with PyTorch.

The model classifies handwritten digit images (0–9) from the MNIST dataset, making it a **multi-class classification task**.

---

# 📊 Dataset

## Name
MNIST Dataset (Modified National Institute of Standards and Technology)

## Type
Grayscale handwritten digit images

## Image Size
28 × 28 pixels

## Classes
10 classes (digits 0–9)

## Source
- https://www.kaggle.com/datasets/oddrationale/mnist-in-csv  
- Also available via `torchvision.datasets.MNIST`

---

# 🔧 Data Preprocessing

## Normalization

Pixel values are normalized to improve training stability:

```python
transforms.Normalize((0.5,), (0.5,))




Reshaping

Since MLP requires 1D input, each image is flattened:

28 × 28 → 784 features
Dataset Split
Training set: 80%
Validation set: 20%
Test set: 10,000 samples
🧠 Model Architecture
Structure

The model is a Multilayer Perceptron (MLP) composed of:

Input layer: 784 neurons
Hidden layers: configurable
Output layer: 10 neurons
Forward Flow
784 → Hidden Layer 1 → Hidden Layer 2 → 10
Activation Functions
ReLU
Tanh
⚙️ Training Setup
Loss Function: CrossEntropyLoss
Optimizer: Adam
Batch Size: 64
Epochs: 10
Device: GPU / CPU
📈 Training Monitoring

During training, the following metrics are tracked:

Training Loss
Training Accuracy
Validation Loss
Validation Accuracy
🧪 Experiments

Two different configurations were tested:

Activation functions
Hidden layer sizes
Learning rates
Experiment Configurations
Experiment	Activation	Hidden Layers	Learning Rate
Experiment 1	ReLU	128 → 64	0.001
Experiment 2	Tanh	256 → 128	0.0005
📊 Results
Experiment	Test Accuracy	Test Loss
Experiment 1	~97%	Lower
Experiment 2	~96%	Higher
📌 Key Observations
ReLU converges faster and performs better
Tanh converges slower and gives slightly lower accuracy
Larger hidden layers increase capacity but also training time
📉 Visualizations

The project includes:

Training Loss vs Epochs
Validation Loss vs Epochs
Training Accuracy vs Epochs
Validation Accuracy vs Epochs

These help analyze:

Model convergence
Overfitting / underfitting
Generalization performance
🧪 Evaluation

The model is evaluated using:

Accuracy (primary metric)
Final test loss

MSE is not used since this is a classification problem.

▶️ How to Run
Install Dependencies
pip install -r requirements.txt
Run Project
Open Jupyter Notebook or Google Colab
Run all cells sequentially
Output

The system will:

Train the MLP model
Run experiments
Display results
Generate plots🚀 Future Improvements
Add Dropout regularization
Apply Batch Normalization
Try deeper architectures
Compare with CNN models
Hyperparameter tuning
👨‍💻 Conclusion

This project demonstrates how a Multilayer Perceptron (MLP) can be used effectively for handwritten digit recognition.

It highlights the impact of:

Network architecture
Activation functions
Learning rate

on model performance and convergence.
