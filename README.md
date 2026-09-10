# Enhanced Attention Transformer U-Net for Kidney Tumour Segmentation Using KiTS23

## Deep Learning-Based 3D Kidney and Kidney Tumour Segmentation from CT Images

This repository contains the complete implementation, experimental workflow, and evaluation framework for the research project:

**"3D Kidney and Kidney Tumour Segmentation Using Deep Learning: A Comparative Study on the KiTS23 Dataset"**

The project investigates automated kidney tumour segmentation from volumetric Computed Tomography (CT) images using advanced deep learning approaches. Three segmentation models are developed and compared:

- **3D U-Net**
- **nnU-Net**
- **Enhanced Attention Transformer U-Net (Proposed Model)**

The aim of this research is to evaluate whether attention-based Transformer mechanisms can improve kidney and tumour segmentation accuracy compared with conventional CNN-based segmentation approaches.

---

# Research Overview

Accurate kidney tumour segmentation from CT images is essential for computer-aided diagnosis, treatment planning, and quantitative medical analysis. However, manual segmentation is time-consuming and affected by tumour variability, irregular boundaries, and anatomical complexity.

This research develops a complete deep learning pipeline consisting of:

- CT data preprocessing
- 3D patch generation
- Deep learning model training
- Segmentation prediction
- Quantitative evaluation
- Qualitative visual analysis

---

# Dataset

## KiTS23 Kidney Tumour Segmentation Dataset

This research uses the publicly available:

**Kidney Tumour Segmentation 2023 (KiTS23) Dataset**

Dataset characteristics:

- Contrast-enhanced CT volumes
- Expert-annotated segmentation masks
- Kidney, tumour, and cyst labels
- 3D volumetric medical imaging data

Dataset Link:

https://kits-challenge.org/kits23/

### Dataset Split

| Dataset | Number of Cases |
|---|---:|
| Training Cases | 489 |
| Testing Cases | 110 |
| Total Cases | 599 |

The dataset contains anonymised medical images and is used only for academic research purposes.

---

# Proposed Methodology

The complete workflow consists of the following stages:




---

# Deep Learning Models

## 1. 3D U-Net

A volumetric extension of the traditional U-Net architecture.

The model uses:

- 3D convolution operations
- Encoder-decoder structure
- Skip connections
- Volumetric feature learning

3D U-Net was implemented as the baseline segmentation model.

---

## 2. nnU-Net

nnU-Net is a self-configuring medical image segmentation framework.

It automatically optimises:

- Data preprocessing
- Network configuration
- Training strategy
- Inference procedures

nnU-Net was used as an advanced benchmark model.

---

## 3. Enhanced Attention Transformer U-Net

The proposed model combines:

- 3D CNN feature extraction
- Attention mechanisms
- Transformer-based global feature learning

The objective is to improve:

- Tumour localisation
- Boundary accuracy
- Complex anatomical feature recognition

---

# Training Configuration

| Parameter | Value |
|---|---|
| Training Cases | 489 |
| Testing Cases | 110 |
| Epochs | 10 |
| Patch Size | 64 × 64 × 64 |
| Optimiser | Adam |
| Learning Rate | 0.0001 |
| Loss Function | Dice Loss + Cross Entropy Loss |

---

# Evaluation Metrics

The models were evaluated using multiple segmentation metrics:

### Dice Similarity Coefficient (DSC)

Measures overlap between predicted segmentation and ground truth.

### Intersection over Union (IoU)

Evaluates segmentation region similarity.

### Precision

Measures correctly predicted positive regions.

### Recall

Measures tumour and kidney detection capability.

### Surface Dice

Evaluates boundary agreement.

### Hausdorff Distance 95 (HD95)

Measures segmentation boundary accuracy.

---

# Experimental Results

The proposed model achieved the best overall segmentation performance.

## Overall Dice Comparison

| Model | Overall Dice |
|---|---:|
| 3D U-Net | 0.758 ± 0.052 |
| nnU-Net | 0.812 ± 0.043 |
| Enhanced Attention Transformer U-Net | **0.852 ± 0.035** |

---

## Kidney and Tumour Segmentation Results

| Model | Kidney Dice | Tumour Dice |
|---|---:|---:|
| 3D U-Net | 0.872 ± 0.041 | 0.642 ± 0.086 |
| nnU-Net | 0.903 ± 0.032 | 0.721 ± 0.074 |
| Enhanced Attention Transformer U-Net | **0.921 ± 0.025** | **0.784 ± 0.061** |

The proposed Enhanced Attention Transformer U-Net achieved improved tumour segmentation performance due to enhanced contextual feature learning through attention mechanisms.

---

# Repository Structure
