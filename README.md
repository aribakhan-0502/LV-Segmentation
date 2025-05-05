# Left Ventricle Segmentation in Echocardiograms using U-Net

![Video Left Ventricle Segmentation/Example Segmentation.png](https://github.com/aribakhan-0502/LV-Segmentation/blob/main/Video%20Left%20Ventricle%20Segmentation/Example%20Segmentation.png)

*Ground truth vs. predicted left ventricle masks*

## Overview
A PyTorch implementation of U-Net for segmenting the left ventricle (LV) in echocardiographic images from the Stanford EchoNet-D dataset. Designed for **GPU-poor environments**, this model achieves real-time inference while preserving clinical accuracy.

## Clinical Motivation
- Automates LV boundary detection for **ejection fraction calculation**.
- Addresses challenges in **low-contrast ultrasound images**.
- Optimized for deployment in resource-constrained clinical settings.

## Key Features
- Encoder-decoder architecture with skip connections  
- Transposed convolutions for upsampling  
- Batch normalization for stable training  

## Performance Metrics

| Metric             | Value       |
|--------------------|-------------|
| Mean IoU           | 74.70%      |
| Dice Coefficient   | 85.20%      |
| Pixel Accuracy     | 97.31%      |
| Inference Time     | 1.15s/frame (T4 GPU) |

## Dataset
**Stanford EchoNet-D**
[Link](https://aimi.stanford.edu/datasets/echonet-dynamic-cardiac-ultrasound)
- 1,000 echocardiogram frames (112×112px) with expert-annotated LV masks  
- Preprocessed to 1 frame per video due to memory constraints  
