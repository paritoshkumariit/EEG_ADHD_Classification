# EEG-Based ADHD Classification Using SE-ResNet1D

## Overview
This project implements deep learning methods to classify Electroencephalography (EEG) signals for distinguishing children with Attention Deficit Hyperactivity Disorder (ADHD) from control subjects. We propose an improved architecture (SE-ResNet1D), leveraging channel-wise attention via Squeeze-and-Excitation (SE) blocks, delivered in a Google Colab notebook format.
- Baseline Models: 1D CNN, ResNet1D
- Proposed Model: SE-ResNet1D (Squeeze-and-Excitation Residual 1D Network)

## Dataset
- Source: [IEEE DataPort - EEG Data for ADHD and Control Children, Nasrabadi et al.]

- Format: MATLAB .mat files

- Channels: 19 electrodes, sampled at 250 Hz

- Subjects: Children diagnosed with ADHD and typically developing controls

- Preprocessing:

  - Bandpass filtering (1-40 Hz, 4th-order Butterworth)

  - Segmentation (1-second, non-overlapping windows)

  - Normalization per segment

  - Data augmentation (Gaussian noise)
 
## Abstract
Electroencephalography (EEG) provides non-invasive insights into neurodevelopmental disorders. This repo explores attention-driven deep learning approaches for ADHD detection, showing that Squeeze-and-Excitation blocks—combined with residual connections—yield state-of-the-art performance on benchmark EEG datasets. The work is inspired and benchmarked against academic literature, including CNN and classical machine learning fusion strategies.

## Methodology
- Preprocessing: Bandpass filtering, segmentation into 1-second windows, normalization

- Augmentation: Gaussian noise

- Model: Squeeze-and-Excitation Residual Network (SE-ResNet1D)

- Training: Adam optimizer, binary cross-entropy

- Evaluation: Accuracy, precision, recall, F1-score, ROC-AUC


## Results Snapshot

| Model |	Accuracy | Approach |
|-------|----------|----------|
| CNN Baseline |	78.54% |	Stacked 1D Convs |
| ResNet1D |	85.0% |	Residual Convs |
| SE-ResNet1D |	88.69% |	Residual + Channel Attention |



  
