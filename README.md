# DSE-Final-Project-CGN
# Counterfactual Generative Networks on Colored MNIST

This repository contains our implementation of **Counterfactual Generative Networks (CGN)** based on the ICLR 2021 paper by Axel Sauer and Andreas Geiger.  
We trained CGNs on a colored MNIST dataset to generate images with disentangled control over shape, texture, and background.

---

## Project Overview

- **Objective**: Generate diverse and interpretable MNIST digits with independent control over visual components.
- **Dataset**: Custom Colored MNIST
- **Main Features**:
  - Counterfactual image generation
  - Shape, texture, and background disentanglement
  - Loss and mask statistics visualization

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/CGN-colored-MNIST.git
cd CGN-colored-MNIST
```

### 2. Install Dependencies

You will need Python 3.7+ and the following packages:

```bash
pip install torch torchvision yacs tqdm matplotlib pillow
```

### 3. Run the Notebook

You can run the project using Jupyter Notebook or Google Colab.

```bash
jupyter notebook CGN_Implementation_1.ipynb
```

---

## How to Reproduce Results

1. **Prepare Data**: The notebook automatically downloads and processes the MNIST dataset, adding random colors.
2. **Train CGN**:
   - Train for 20 epochs with a batch size of 64.
   - Generator and Discriminator losses are tracked.
   - Images and statistics are saved periodically.
3. **Visualizations**:
   - Generated images show the variety in shapes, textures, and backgrounds.
   - Loss curves display training stability.
   - Mask statistics show the diversity in generated masks.

---

## Output Examples

- **Generated Images**: Variety of MNIST digits with diverse appearances.
- **Training Losses**: Generator stabilizes around 7.5-8, Discriminator stays low (~0.2).
- **Mask Statistics**: Mean between 0.20–0.45, Variance between 0.16–0.22, indicating healthy mask generation.

---

## References

- Sauer, A., & Geiger, A. (2021). [Counterfactual Generative Networks](https://arxiv.org/abs/2101.06046). ICLR.
- LeCun, Y. et al. (1998). Gradient-based learning for document recognition (MNIST).
- Goodfellow, I. et al. (2014). Generative Adversarial Nets.
- Simonyan, K., & Zisserman, A. (2014). Very Deep Convolutional Networks for Large-Scale Image Recognition (VGG for Perceptual Loss).
