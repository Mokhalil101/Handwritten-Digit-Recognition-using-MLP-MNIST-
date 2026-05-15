# Handwritten Digit Recognition using Multilayer Perceptron (MLP)

## 📌 Problem Description
This project aims to build a **Handwritten Digit Recognition system** using a **Multilayer Perceptron (MLP)** neural network.  
The model classifies handwritten digit images (0–9) from the MNIST dataset into their corresponding classes.

The task is formulated as a **multi-class classification problem** with 10 output classes.

---

## 📊 Dataset
- **Dataset Name:** MNIST (Modified National Institute of Standards and Technology)
- **Type:** Grayscale images
- **Image Size:** 28 × 28 pixels
- **Number of Classes:** 10 (digits 0–9)

### Dataset Link
https://www.kaggle.com/datasets/oddrationale/mnist-in-csv  
(Also loaded directly using PyTorch `torchvision.datasets.MNIST`)

---

## 🔧 Data Preprocessing
The following preprocessing steps were applied:

- **Missing Values:**  
  The MNIST dataset does not contain missing values, so no handling was required.

- **Normalization:**  
  Pixel values were normalized using:

Normalize(mean=0.5, std=0.5)


- **Reshaping:**  
Images were flattened from 28×28 to 784-dimensional vectors to be compatible with the MLP input layer.

- **Encoding:**  
Labels are already encoded as integers (0–9), so no additional encoding was needed.

- **Data Split:**  
- Training set: 60,000 samples  
- Testing set: 10,000 samples  

---

## 🧠 Model Architecture (MLP)
The implemented model is a **Multilayer Perceptron** consisting of:

- Input Layer: 784 neurons  
- Hidden Layers: Variable (based on experiment)  
- Output Layer: 10 neurons  

### General Architecture

Input (784)
→ Hidden Layer 1
→ Hidden Layer 2
→ Output (10)


---

## ⚙️ Training Configuration
- **Loss Function:** CrossEntropyLoss  
- **Optimizer:** Adam  
- **Batch Size:** 64  
- **Epochs:** 10  
- **Device:** GPU (if available) / CPU  

During training, the following metrics were monitored:
- Training Loss
- Training Accuracy

---

## 🧪 Experiments (Mandatory Requirement)

Two experiments were conducted by varying:
- Activation function
- Number of neurons
- Learning rate

### 🔹 Experiment Settings

| Experiment | Activation | Hidden Layers | Learning Rate |
|----------|-----------|---------------|---------------|
| Experiment 1 | ReLU | 128 → 64 | 0.001 |
| Experiment 2 | Tanh | 256 → 128 | 0.0005 |

---

## 📈 Results

| Experiment | Test Accuracy | Test Loss |
|----------|---------------|-----------|
| Experiment 1 (ReLU) | ~97% | Lower |
| Experiment 2 (Tanh) | ~96% | Higher |

### Observations
- ReLU achieved faster convergence and higher accuracy.
- Tanh showed slower learning and slightly lower performance.
- Increasing the number of neurons increased model capacity but also training time.

---

## 📉 Visualization
The following plots are included:
- Training Loss vs Epochs (for both experiments)
- Training Accuracy vs Epochs (for both experiments)

These visualizations help compare convergence behavior and performance stability.

---

## 🧪 Evaluation
The model was evaluated on the test dataset using:
- **Accuracy** (classification metric)
- **Final Loss Value**

> Mean Squared Error (MSE) was not used because the problem is a classification task, not regression.
## ▶️ How to Run the Project
1. Open Google Colab or local environment
2. Install dependencies:
```bash
pip install torch torchvision matplotlib
Run the notebook cells sequentially
Training and evaluation results will be displayed automatically
✅ Conclusion

This project successfully demonstrates the use of a Multilayer Perceptron for handwritten digit recognition.
Experimentation shows that activation functions and network size significantly impact performance.

Future improvements may include:

Adding Dropout for regularization
Trying Batch Normalization
Increasing number of experiments
