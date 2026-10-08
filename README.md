# Underwater Ship Hull Inspection Using Semantic Segmentation with Deep Learning Models

## Overview

This project focuses on automated underwater ship hull inspection using semantic segmentation and deep learning.

The project uses the LIACi dataset to segment different regions and components of ship hulls from underwater images.

## Models

Two segmentation models were implemented and evaluated:

### 1. U-Net + MobileNetV2

U-Net with a MobileNetV2 backbone was implemented as a lightweight segmentation model for comparison.

Different improvements were explored, including improved training, class weighting and Test-Time Augmentation (TTA).

The best result obtained was:

- **mIoU:** 47.19%
- **Dice:** 58.42%

### 2. PSPNet + ResNet50

PSPNet with a ResNet50 backbone was developed as the **proposed model**.

The model was improved using:

- Focal Loss + Dice Loss
- Test-Time Augmentation (TTA)

The best result obtained was:

- **mIoU:** 56.52%
- **Dice:** 70.50%

## Dataset

The project uses the **LIACi underwater ship hull inspection dataset**.

The segmentation task includes the following classes:

- Void
- Ship Hull
- Marine Growth
- Anode
- Overboard Valve
- Propeller
- Paint Peel
- Bilge Keel
- Defect
- Corrosion
- Sea Chest Grating

## Explainable AI

Grad-CAM was integrated with the proposed **PSPNet + ResNet50** model to visualize the regions influencing the model's predictions.

Class-specific Grad-CAM explanations were generated and combined with the segmentation results to provide a visual interpretation of the model's predictions.

## VLM Integration

A Vision-Language Model (VLM) is being integrated with the proposed PSPNet pipeline to provide human-readable analysis of underwater ship hull segmentation and inspection results.

The planned workflow is:

Underwater Image  
↓  
PSPNet + ResNet50  
↓  
Semantic Segmentation  
↓  
Grad-CAM / XAI  
↓  
VLM Analysis  
↓  
Inspection-oriented Explanation

## Project Structure

```text
Ship_Hull-Semantic-Segmentation/
│
├── PSPNet_XAI.ipynb
├── README.md
└── ...
