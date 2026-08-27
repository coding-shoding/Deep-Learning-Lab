# Lab 01: Single Layer Perceptron (SLP)

## Overview
Implementation and analysis of a Single Layer Perceptron (SLP) for binary classification on the Banknote Authentication dataset as part of the CS3807 Deep Learning Laboratory.

The lab covers building an SLP from scratch using NumPy, evaluating convergence across different learning rates, comparing with scikit-learn, and demonstrating why a single perceptron cannot solve non-linear problems like XOR.

---

## Author Information
- **Student Name**: Atiksh Borundia
- **Registration Number**: 24011101009
- **Degree**: B.Tech. Artificial Intelligence & Data Science
- **Institution**: Shiv Nadar University Chennai
- **Course**: CS3807 — Deep Learning Laboratory

---

## Lab Files
- `dl_lab1_single_perceptron.py`: Complete Python source code.
- `CS3807_Lab01_Single_Layer_Perceptron_Report.pdf`: Lab report with plots and observations.

---

## Dataset: Banknote Authentication
- **Source**: UCI Machine Learning Repository (ID 267)
- **Samples**: 1,372 instances
- **Classes**: 2 (Authentic: 762, Forged: 610)
- **Features**: Variance, Skewness, Curtosis, Entropy (from Wavelet transformed images)

---

## Key Tasks & Methodology
1. **Exploratory Data Analysis**: Inspected feature distributions, summary statistics, and correlation heatmaps.
2. **Preprocessing**: Normalized features using StandardScaler and split data into 80% train / 20% test sets.
3. **Perceptron from Scratch**: Implemented the linear combination and unit step activation with iterative weight updates.
4. **Training & Convergence**: Tracked training error across epochs until convergence.
5. **Hyperparameter Analysis**: Evaluated convergence speed across learning rates (0.0001 to 1.0) and tested step vs. sigmoid activations.
6. **XOR Problem Demonstration**: Verified that SLP succeeds on linearly separable logic (AND, OR) but fails on XOR.
7. **Benchmarking**: Compared accuracy and metrics against scikit-learn's Perceptron.

---

## Results Summary
- **Accuracy**: ~99% on the test set.
- **Precision / Recall / F1-Score**: > 0.98 for both classes.
- **Convergence**: Normalizing features reduced convergence time by over 60%.
- **XOR Outcome**: Confirmed that a single-layer perceptron cannot form non-linear decision boundaries, requiring multi-layer architectures.

---

## How to Run
From this folder:
```bash
python dl_lab1_single_perceptron.py
```
Output plots and summary CSVs are automatically saved in `plots/` and `results/` folders.
