# Lab 02: Multi-Layer Perceptron (MLP)

## Overview
Implementation, training, and evaluation of a Multi-Layer Perceptron (MLP) for multi-class image classification on Fashion-MNIST using TensorFlow/Keras for the CS3807 Deep Learning Laboratory.

The experiment explores data preprocessing, feedforward architectures, systematic hyperparameter optimization (learning rate, optimizers, batch size), error analysis via confusion matrix, and solving the non-linear XOR problem using an MLP.

---

## Author Information
- **Student Name**: Atiksh Borundia
- **Registration Number**: 24011101009
- **Degree**: B.Tech. Artificial Intelligence & Data Science
- **Institution**: Shiv Nadar University Chennai
- **Course**: CS3807 — Deep Learning Laboratory

---

## Lab Files
- `dl_lab2_multi_layered_perceptron.py`: Complete Python source code.
- `CS3807_Lab02_Multi_Layer_Perceptron_Report.pdf`: Lab report with hyperparameter tables, loss curves, and analysis.

---

## Dataset: Fashion-MNIST
- **Total Images**: 70,000 grayscale images (28x28 pixels)
- **Split**: 60,000 training, 10,000 testing
- **Classes**: 10 clothing categories (T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot)
- **Balance**: 6,000 images per class

---

## Model Architecture & Tasks
1. **Preprocessing**: Flattened 28x28 images to 784-dimensional vectors, scaled pixel values to [0, 1], and converted labels to one-hot vectors.
2. **Network Architecture**:
   - Input: 784 features
   - Hidden Layer 1: 128 neurons (ReLU activation)
   - Hidden Layer 2: 64 neurons (ReLU activation)
   - Output Layer: 10 neurons (Softmax activation)
3. **Training**: Categorical cross-entropy loss with Adam optimizer and validation monitoring.
4. **Hyperparameter Tuning**:
   - Learning rates: 0.0001, 0.001, 0.01, 0.1
   - Optimizers: Adam, SGD, RMSprop
   - Batch sizes: 16, 32, 64, 128
   - Hidden layer capacities
5. **XOR Resolution**: Built a small 2-layer MLP to empirically demonstrate how non-linear hidden representations solve the XOR problem.

---

## Results Summary
- **Baseline Accuracy**: ~88.4%
- **Optimized Accuracy**: ~89.5%
- **Optimizer Comparison**: Adam delivered faster convergence and superior stability compared to SGD and RMSprop.
- **Classification Insights**: Footwear classes (Sneakers, Boots) achieved high accuracy (>95%), while visually similar upper-body garments (Shirts vs. T-shirts) accounted for most misclassifications.

---

## How to Run
From this folder:
```bash
python dl_lab2_multi_layered_perceptron.py
```
