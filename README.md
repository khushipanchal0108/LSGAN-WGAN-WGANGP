Got it — here's the same content, fully rephrased **without emojis** and with a clean, professional tone suitable for your assignment or GitHub README:

---

# LSGAN vs WGAN vs WGAN-GP: Comparative Analysis for Pneumonia X-ray Generation

## Overview

This project presents a comparative analysis of three Generative Adversarial Network (GAN) variants—Least Squares GAN (LSGAN), Wasserstein GAN (WGAN), and Wasserstein GAN with Gradient Penalty (WGAN-GP)—using the PneumoniaMNIST dataset. The primary aim is to evaluate how effectively each model can generate realistic chest X-ray images for pneumonia detection, using standard performance metrics such as Inception Score (IS) and Fréchet Inception Distance (FID).

---

## Objective

Generative models have proven useful in the medical imaging domain for data augmentation, anomaly detection, and synthetic image generation. This study investigates the effectiveness of the following GAN models:

- **LSGAN**: Uses a least-squares loss function to encourage stable training and generate more realistic images.
- **WGAN**: Implements Wasserstein distance for improved convergence and better learning dynamics.
- **WGAN-GP**: Enhances WGAN by adding a gradient penalty to enforce Lipschitz continuity, addressing issues like mode collapse and unstable training.

---

## Dataset: PneumoniaMNIST

- **Source**: MedMNIST benchmark suite for lightweight medical image analysis tasks.
- **Image Type**: 28×28 grayscale chest X-ray images.
- **Classification**: Binary (Pneumonia vs Normal)
- **Dataset Size**:
  - Training set: 5,856 images
  - Validation set: 1,496 images
  - Test set: 1,498 images

### Citation

If you use this dataset, please cite the following works:

- Yang, Jiancheng, et al. *"MedMNIST v2 - A large-scale lightweight benchmark for 2D and 3D biomedical image classification."* Scientific Data, 2023.
- Yang, Jiancheng, et al. *"MedMNIST Classification Decathlon."* IEEE ISBI, 2021.

---

## Methodology

- **Network Architecture**: All three GAN variants use the same generator and discriminator architecture to ensure fair comparison.
- **Training Details**:
  - Number of epochs: 50
  - Optimizer: Adam with tuned hyperparameters specific to each model
  - Environment: Google Colab with GPU acceleration
- **Evaluation Metrics**:
  - **Inception Score (IS)** – Measures image diversity and quality.
  - **Fréchet Inception Distance (FID)** – Measures the similarity between synthetic and real image distributions.

---

## Results (at Epoch 50)

| Model     | Inception Score (↑) | FID Score (↓) |
|-----------|----------------------|---------------|
| LSGAN     | 1.6420               | 26.5000       |
| WGAN      | 1.9418               | 26.5000       |
| WGAN-GP   | 1.4848               | 26.5000       |

- **IS (Inception Score)**: A higher score suggests better image diversity and visual quality.
- **FID (Fréchet Inception Distance)**: A lower score indicates the generated images are more similar to real ones.

---

## Key Observations

- **WGAN** achieved the highest Inception Score, indicating better diversity and realism among the generated images.
- **LSGAN** performed reasonably well, ranking between WGAN and WGAN-GP.
- **WGAN-GP** had the lowest IS score, but the differences were not drastic.
- All models obtained the same FID score, suggesting that their outputs were similarly close to the distribution of real images.

---
##Tensorboard Results

![Screenshot 2025-04-11 183830](https://github.com/user-attachments/assets/b7fc4629-5b4b-4de6-b60b-734bcd2d5cc6)

![Screenshot 2025-04-11 183900](https://github.com/user-attachments/assets/a2804ebb-3009-45b7-83b5-8ec650996299)

![Screenshot 2025-04-11 184036 - Copy](https://github.com/user-attachments/assets/e5e87324-bcff-4932-8ee3-77dc9b86a107)

![Screenshot 2025-04-11 184102](https://github.com/user-attachments/assets/ea1b2a64-f8cd-4d82-9116-f04d17ec23ac)

![Screenshot 2025-04-11 184119](https://github.com/user-attachments/assets/0cea0905-4650-4550-9d3d-d4b36abbe289)

