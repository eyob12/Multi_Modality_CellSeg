# Multi-Modality Cell Segmentation 
A universal cell segmentation model designed to accurately segment cells of varying shapes across a wide range of multimodality microscopic images, including brightfield, fluorescent, phase contrast (PC), and differential interference contrast (DIC) modalities.

This repository contains the implementation of a novel Multi-Modality Cell Segmentation framework.
## Code Availability
The source code for this repository will be made publicly available upon the acceptance of the associated research paper. Stay tuned for updates!
## Overview of Methodology
![sample_methodology6](https://github.com/user-attachments/assets/522fb8b0-d593-4705-a0c0-9abbd11ba9d0)

## Key Features
### Image Standardization Module
[X] Resolves multi-modality heterogeneity by unifying inputs into consistent spatial and channel dimensions
### Shape-Aware Classification
[X] Classify the dataset into five classes based on  shape information such as round, tiny/tightly
packed, irregular, elongated, and clustered/densely packed forms.
### Auto-Point Prompt Generation (APPGen)
[X] Eliminates manual prompting by automating point prompt generation
###  Boundary-Aware SAM Adaptation
[X] Integrates distance maps during fine-tuning and optimizes segmentation performance through global pixel intensity preservation and local edge detail enhancement.

