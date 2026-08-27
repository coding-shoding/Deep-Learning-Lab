# Lab 03: Convolutional Neural Networks (CNNs)

## Overview
Implementation, training, and analysis of Convolutional Neural Networks (CNNs) for image classification on CIFAR-10 using TensorFlow/Keras for the CS3807 Deep Learning Laboratory.

The experiment explores convolution arithmetic, feature map extraction, Max Pooling vs. Average Pooling comparisons, filter scaling effects, and end-to-end model evaluation.

---

## Author Information
- **Student Name**: Atiksh Borundia
- **Registration Number**: 24011101009
- **Degree**: B.Tech. Artificial Intelligence & Data Science
- **Institution**: Shiv Nadar University Chennai
- **Course**: CS3807 — Deep Learning Laboratory

---

## Lab Files
- `experiment_3_cnn_cifar10.py`: Complete Python source code.
- `CS3807_Lab03_Convolutional_Neural_Networks_Report.pdf`: Lab report with feature maps, confusion matrix, and derivations.

---

## Dataset: CIFAR-10
- **Total Images**: 60,000 color images (32x32 pixels, 3 channels)
- **Split**: 50,000 training, 10,000 testing
- **Classes**: 10 categories (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)
- **Balance**: 6,000 images per class

---

## Model Architecture & Tasks
1. **Convolution Mechanics**: Applied Conv2D layers with varying kernel sizes (3x3, 5x5), strides, and padding options (valid vs. same).
2. **Feature Map Visualization**: Extracted and inspected activations from early filters to observe edge, texture, and color detection.
3. **Pooling Study**: Compared Max Pooling vs. Average Pooling in terms of dimensionality reduction and validation accuracy.
4. **End-to-End CNN Architecture**:
   - Conv2D (32 filters, 3x3, same, ReLU) -> MaxPooling2D (2x2)
   - Conv2D (64 filters, 3x3, same, ReLU) -> MaxPooling2D (2x2)
   - Flatten -> Dense (128, ReLU) -> Dense (10, Softmax)
5. **Additional Exercises**:
   - Parameter counting for RGB convolutional layers.
   - Comparison of ReLU vs. Sigmoid activations.
   - Filter scaling analysis (16 vs. 64 filters) measuring accuracy vs. runtime.

---

## Results Summary
- **Test Accuracy**: ~72% on CIFAR-10 test set.
- **Pooling Comparison**: Max Pooling achieved better feature retention and higher validation accuracy (~64.2%) than Average Pooling (~61.8%).
- **Filter Capacity**: Increasing filters from 16 to 64 improved classification accuracy while increasing per-epoch training time.
- **Class Performance**: Vehicles (Automobile, Ship) achieved strong separability, while animal classes (Cat, Dog) had higher mutual confusion due to low-resolution texture similarities.

---

## How to Run
From this folder:
```bash
python experiment_3_cnn_cifar10.py
```
Generated artifacts include `feature_maps.png` and `activation_comparison.png`.
