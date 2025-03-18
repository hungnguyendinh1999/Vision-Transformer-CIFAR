# Vision Transformer (ViT) for CIFAR-10 Classification  

This repository contains an implementation of a Vision Transformer (ViT) for image classification on the CIFAR-10 dataset. The model is implemented from scratch using PyTorch and trained under specific constraints. 

NOTE: If I missed anything, please let me know!

## Task Overview  
The goal of this project is to implement a Vision Transformer (ViT) variant using a **pre-norm Transformer cell**, as described in [Dosovitskiy et al., 2020, An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/pdf/2010.11929). The model is trained on **CIFAR-10** and must achieve at least **50% validation accuracy** within **3 training epochs**, without using pre-trained weights.

## Implementation Details
- **Architecture**:  
  - A variant of the **pre-norm Transformer cell** (post-norm does not perform well in this setting).  
  - The number of model parameters is **less than 3.2 million**.  
  - No pre-trained weights are used; training is done **from scratch**.  
  - The model is trained using **only 3 epochs**.  
<img width="675" alt="Vision Transformer Architecture from the original paper" src="https://github.com/user-attachments/assets/82802140-b91c-4710-a147-b7965d98d93e" />

- **Dataset**:  
  - CIFAR-10, a dataset of 60,000 32x32 color images across 10 classes.  
  - The dataset is loaded and preprocessed using standard normalization and augmentation techniques.  

- **Training Constraints**:  
  - The model must be implemented without modifying previous function definitions (new functions are re-implemented as needed).  
  - Achieving at least **50% validation accuracy** is required for full credit.  

## Dependencies
At the time of running this, I was using `python=3.11`

Ensure you have the following dependencies installed before running the notebook:  
```bash
pip install torch torchvision numpy matplotlib
```
