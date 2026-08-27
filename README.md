# CS3807: Deep Learning Laboratory

## Overview
This repository contains code implementations, experimental evaluations, and formal reports for the CS3807 Deep Learning Laboratory at Shiv Nadar University Chennai.

The project is organized in a modular structure to accommodate both current foundational labs and future advanced architectures.

---

## Author & Academic Information
- **Student Name**: Atiksh Borundia
- **Registration Number**: 24011101009
- **Department**: Artificial Intelligence & Data Science
- **Institution**: Shiv Nadar University Chennai
- **Course**: CS3807 — Deep Learning Laboratory

---

## Repository Structure
```
dl/
├── README.md                                           # Master course repository overview
├── requirements.txt                                    # Python dependencies
│
├── Lab-01-Single-Layer-Perceptron/
│   ├── README.md                                       # Lab 1 documentation
│   ├── dl_lab1_single_perceptron.py                    # SLP source code
│   └── CS3807_Lab01_Single_Layer_Perceptron_Report.pdf  # Lab report
│
├── Lab-02-Multi-Layer-Perceptron/
│   ├── README.md                                       # Lab 2 documentation
│   ├── dl_lab2_multi_layered_perceptron.py             # MLP source code
│   └── CS3807_Lab02_Multi_Layer_Perceptron_Report.pdf  # Lab report
│
├── Lab-03-Convolutional-Neural-Networks/
│   ├── README.md                                       # Lab 3 documentation
│   ├── experiment_3_cnn_cifar10.py                     # CNN source code
│   └── CS3807_Lab03_Convolutional_Neural_Networks_Report.pdf # Lab report
│
└── [Future-Labs]/                                      # Slots for upcoming labs
    ├── README.md
    ├── lab_script.py
    └── CS3807_LabXX_Topic_Report.pdf
```

---

## Curriculum Index & Progress

| Lab | Experiment Title | Paradigm / Key Concept | Dataset | Status |
| :---: | :--- | :--- | :--- | :---: |
| **01** | Single Layer Perceptron (SLP) | From-scratch Perceptron, Convergence, XOR Problem | Banknote Authentication | Completed |
| **02** | Multi-Layer Perceptron (MLP) | Deep Feedforward, Hyperparameter Tuning, XOR Solution | Fashion-MNIST | Completed |
| **03** | Convolutional Neural Networks (CNNs) | Convolutions, Pooling Comparison, Feature Maps | CIFAR-10 | Completed |
| **04** | Recurrent Neural Networks (RNNs / LSTMs) | Sequence Modeling, Temporal Dynamics | Planned | Upcoming |
| **05** | Attention & Transformers | Self-Attention, Sequence-to-Sequence Modeling | Planned | Upcoming |
| **06** | Autoencoders & Representation Learning | Dimensionality Reduction, Latent Representations | Planned | Upcoming |
| **07** | Generative Adversarial Networks (GANs) | Adversarial Training, Image Generation | Planned | Upcoming |

---

## Adding Future Labs
To add new labs while preserving consistency:
1. Create a folder named `Lab-<XX>-<Lab-Title>`
2. Include the source code script (`.py` or `.ipynb`)
3. Include the lab report PDF named `CS3807_Lab<XX>_<Topic>_Report.pdf`
4. Add a concise `README.md` summarizing objectives, dataset, architecture, and key results
5. Update the Curriculum Index table above to mark the lab as Completed

---

## Setup & Execution
1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run any experiment by navigating into its folder:
```bash
# Example for Lab 1
cd Lab-01-Single-Layer-Perceptron
python dl_lab1_single_perceptron.py
```
