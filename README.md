# 🧠 Handwritten Digit Recognition using Multilayer Perceptron (MLP)

## 🚀 Project Overview
This project implements a **Handwritten Digit Recognition system** using a **Multilayer Perceptron (MLP)** built with PyTorch.

The model classifies grayscale images of handwritten digits (0–9) from the MNIST dataset into 10 classes, making it a **multi-class classification problem**.

---

## 📊 Dataset

- **Dataset Name:** MNIST (Modified National Institute of Standards and Technology)
- **Type:** Grayscale images
- **Image Size:** 28 × 28 pixels
- **Number of Classes:** 10 (digits 0–9)

### 📥 Dataset Source
- Kaggle Dataset:  
  https://www.kaggle.com/datasets/oddrationale/mnist-in-csv  
- Also loaded using:
  `torchvision.datasets.MNIST`

---

## 🔧 Data Preprocessing

### ✔ Normalization
```python
Normalize(mean=0.5, std=0.5)
✔ Reshaping

Images are flattened from:

28 × 28 → 784 features
✔ Data Split
Training Set: 80%
Validation Set: 20%
Test Set: 10,000 samples
🧠 Model Architecture (MLP)
Input Layer: 784 neurons
Hidden Layers: Configurable (based on experiment)
Output Layer: 10 neurons
📌 Architecture Flow
784 → Hidden Layer 1 → Hidden Layer 2 → 10
🔥 Activation Functions Used
ReLU
Tanh
⚙️ Training Configuration
Loss Function: CrossEntropyLoss
Optimizer: Adam
Batch Size: 64
Epochs: 10
Device: GPU (if available) / CPU
📈 Metrics Tracked

During training:

Training Loss
Training Accuracy
Validation Loss
Validation Accuracy
🧪 Experiments

Two experiments were conducted by varying:

Activation function
Number of neurons
Learning rate
🔬 Experiment Settings
Experiment	Activation	Hidden Layers	Learning Rate
Experiment 1	ReLU	128 → 64	0.001
Experiment 2	Tanh	256 → 128	0.0005
📊 Results
Experiment	Test Accuracy	Test Loss
Experiment 1 (ReLU)	~97%	Lower
Experiment 2 (Tanh)	~96%	Higher
📌 Observations
ReLU converges faster and achieves better performance.
Tanh shows slower convergence and slightly lower accuracy.
Increasing hidden layer size improves model capacity but increases training time.
📉 Visualizations

The following plots are generated:

Training Loss vs Epochs
Validation Loss vs Epochs
Training Accuracy vs Epochs
Validation Accuracy vs Epochs
🎯 Purpose

These visualizations help analyze:

Model convergence behavior
Overfitting / underfitting
Performance stability across experiments
🧪 Evaluation

The model was evaluated using:

Accuracy (classification metric)
Final Test Loss

Note: Mean Squared Error (MSE) is not used because this is a classification problem.

▶️ How to Run the Project
1️⃣ Install Dependencies

All required libraries are listed in:

requirements.txt

Install them using:

pip install -r requirements.txt
2️⃣ Run the Project
Open Google Colab or local environment
Run all cells sequentially
3️⃣ Output

The system will:

Train the MLP model
Run experiments
Display results
Generate comparison plots

🧠 Key Insights
ReLU performs better than Tanh due to reduced vanishing gradient problem.
Increasing hidden layers improves learning capacity but increases computation cost.
Validation monitoring is essential for generalization performance.
🚀 Future Improvements
Add Dropout regularization
Apply Batch Normalization
Try deeper architectures
Compare with CNN models
Hyperparameter tuning (Grid Search / Random Search)
👨‍💻 Conclusion

This project demonstrates the effectiveness of a Multilayer Perceptron (MLP) for handwritten digit recognition using the MNIST dataset.

It shows how:

Architecture design
Activation functions
Learning rate

significantly impact model performance.
