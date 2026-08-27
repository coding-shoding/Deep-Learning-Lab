# Lab 04: Comparative Study of Deep CNN Architectures Using Transfer Learning

## Overview
Comparative study of deep convolutional neural network architectures and transfer learning methodologies for image classification on CIFAR-10 for the CS3807 Deep Learning Laboratory.

The experiment evaluates training smaller CNNs from scratch (LeNet-5, adapted AlexNet) versus applying transfer learning with pretrained ImageNet backbones (VGG16, ResNet50, InceptionV3, MobileNetV2), analyzing feature extraction vs. fine-tuning, parameter efficiency, and hyperparameter tuning.

---

## Author Information
- **Student Name**: Atiksh Borundia
- **Registration Number**: 24011101009
- **Degree**: B.Tech. Artificial Intelligence & Data Science
- **Institution**: Shiv Nadar University Chennai
- **Course**: CS3807 — Deep Learning Laboratory

---

## Lab Files
- `experiment_4_cifar10_transferlearning_final.py`: Complete Python source code.
- `CS3807_Lab04_Transfer_Learning_Report.pdf`: Formal lab report with comparative tables, confusion matrices, and analysis.

---

## Dataset: CIFAR-10
- **Total Images**: 60,000 color images (32x32 pixels, 3 channels)
- **Split**: 50,000 training, 10,000 testing
- **Classes**: 10 categories (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)
- **Preprocessing**: Scaled to [0, 1] and dynamically upsampled to 96x96 for pretrained ImageNet backbones.

---

## Evaluated Architectures & Methodology
1. **Scratch Architectures**:
   - **LeNet-5**: Classic early CNN architecture with two conv-pool stages and dense layers.
   - **AlexNet (Adapted)**: Deep 5-stage convolutional feature extractor with Dropout and dense classification heads.
2. **Pretrained Transfer Learning Backbones**:
   - **VGG16**: Deep uniform 3x3 convolutions with frozen base and custom classification head.
   - **ResNet50**: Residual skip-connections addressing vanishing gradients in deep networks.
   - **InceptionV3 / GoogleNet**: Multi-scale parallel convolutional factorization.
   - **MobileNetV2**: Efficient depthwise separable convolutions and inverted residuals.
3. **Training Paradigms**:
   - **Feature Extraction**: Base model frozen; only top classification layers trained.
   - **Fine-Tuning**: Top convolutional blocks unfrozen and trained with a reduced learning rate.
4. **Hyperparameter Study**:
   - Tested variations in learning rate, batch size, optimizers (Adam vs. SGD), dense layer capacity, and number of frozen layers.

---

## Results Summary
- **Transfer Learning Superiority**: Pretrained models (VGG16, ResNet50) achieved higher test accuracy (>82–88%) compared to scratch models trained on CIFAR-10 (~62–73%), benefiting from rich ImageNet feature representations.
- **Fine-Tuning Gain**: Unfreezing top convolutional blocks yielded an additional 3–5% accuracy boost over pure feature extraction.
- **Efficiency Trade-offs**: MobileNetV2 offered the best balance between parameter efficiency, fast inference, and high classification accuracy.

---

## How to Run
From this folder:
```bash
python experiment_4_cifar10_transferlearning_final.py
```
Outputs and comparative metrics are saved automatically.
