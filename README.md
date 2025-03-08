# Multi-Modality Cell Segmentation 
A universal cell segmentation model designed to accurately segment cells of varying shapes across a wide range of multimodality microscopic images, including brightfield, fluorescent, phase contrast (PC), and differential interference contrast (DIC) modalities.

This repository contains the implementation of a novel Multi-Modality Cell Segmentation framework.
## Code Availability
The source code for this repository will be made publicly available upon the acceptance of the associated research paper. Stay tuned for updates!
## Overview of Methodology
![sample_methodology6](https://github.com/user-attachments/assets/522fb8b0-d593-4705-a0c0-9abbd11ba9d0)

## Key Features
### 1. Image Standardization Module
- [X] Resolves multi-modality heterogeneity by unifying inputs into consistent spatial and channel dimensions
### 2. Shape-Aware Classification
- [X] Classify the dataset into five classes based on  shape information such as round, tiny/tightly
packed, irregular, elongated, and clustered/densely packed forms.
### 3. Auto-Point Prompt Generation (APPGen)
- [X] Eliminates manual prompting by automating point prompt generation
###  4. Boundary-Aware SAM Adaptation
- [X] Integrates distance maps during fine-tuning and optimizes segmentation performance through global pixel intensity preservation and local edge detail enhancement.

## Results
Our proposed model was trained on OmniPose, CellPose, Sartorius, and CellSeg Challenge datasets. We evaluate the performance of our model on NeurIPS Cell Segmentation Challenge test datasets.
<img src="![2Sample_Result_SegModel](https://github.com/user-attachments/assets/e4ae2111-4cac-47f7-bbed-107a5604d068)" alt="Proposed segmentation model performance on different multi-modality data and classes." width="800"/>

## Comparation
![comaparation3](https://github.com/user-attachments/assets/ad9811bf-afe9-4729-9aa7-84b246322c82)

For more details, refer to the [documentation](#documentation).


## Repository Structure

- **preprocessing**  
  Contains scripts for refining ground truth to a distance map and multi-modality image standardization.

- **training.ipynb**  
  Jupyter Notebook for training the multi-modality cell Segmentation model.

- **test.ipynb**  
  Jupyter Notebook for testing the multi-modality cell Segmentation model.

- **Saved_model**  
  Pretrained models.

- **evaluation**  
  Scripts for calculating evaluation metrics such as MSE, IoU, F1, and PQ.

- **datasets**  
  Scripts for dataset preparation.

---
## Installation

Clone the repository:  
```bash
git clone https://github.com/eyob12/Multi_Modality_CellSeg.git 
cd Multi_Modality_CellSeg 

```
## Install Dependencies
  
Install the required Python dependencies:\  
```bash
 pip install -r requirements.txt 


```
# Usage
## Data Preprocessing
Use the provided script to apply refining ground truth and image standardization:
```bash
python preprocess.py --input_dir <path-to-dataset> --output_dir <path-to-output>

```
## Train the Model
Start training with:
```bash
python train.py --config config.yaml
```
## Evaluate the Model
Evaluate on test datasets with:
```bash
python evaluate.py --weights <path-to-weights>
```
# Citation 
```bash
