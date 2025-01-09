# Polyp-PVT Implementation (Study & Learning Purposes)

Comparative Study Paper here: https://drive.google.com/file/d/1LoTorOhbqq1G_NBc4Vw6BAG8TmCaf5xu/view?usp=drive_link

This repository is a personal implementation of the paper **"Polyp-PVT: Polyp Segmentation with Pyramid Vision Transformers"** by Bo Dong, Wenhai Wang, Jinpeng Li, and Deng-Ping Fan. I created this repo for study and learning purposes, with minor custom modifications to help me better understand the model and experiment with it. Original Repo  here: https://github.com/DengPingFan/Polyp-PVT

The original implementation is based on the **Polyp-PVT** model, which uses **Pyramid Vision Transformers (PVT)** for polyp segmentation. My modifications are intended to assist in experimenting with the methodology and understanding how the model performs in different configurations.

## 1. Introduction

**Polyp-PVT** is a cutting-edge method for polyp segmentation using transformer architecture. Unlike traditional CNN-based methods, Polyp-PVT utilizes a transformer encoder, which improves the exchange of information between the encoder and decoder. It introduces three key modules to enhance segmentation accuracy:

- **Cascaded Fusion Module (CFM)**: Collects high-level semantic and location information of polyps.
- **Camouflage Identification Module (CIM)**: Detects polyp information hidden in low-level features.
- **Similarity Aggregation Module (SAM)**: Extends pixel features with high-level semantic position information to better fuse features across different levels.

The model has shown strong performance in both image-level and video-level polyp segmentation:

- **Image-level Polyp Segmentation**: 0.808 mean Dice, 0.727 mean IoU on ColonDB
- **Video-level Polyp Segmentation**: 0.880 mean Dice, 0.802 mean IoU on CVC-300-TV

## 2. Modifications for Study and Learning

To aid in my learning, I made the following custom modifications to the original implementation:

1. **Custom Dataset Loader**: Adapted the data pipeline to work with custom polyp datasets for testing and experimentation.
2. **Hyperparameter Tweaks**: Adjusted hyperparameters such as learning rate and batch size to explore their impact on model performance.
4. **Simplified Training Loop**: Modified the training loop for easier model checkpointing and more detailed logging, helping with my analysis.
5. **Explored option for Pretrained Weights for Fine-Tuning**: Explored an option to fine-tune the model on new datasets using pretrained weights.

## 3. Usage

1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd Polyp-PVT
