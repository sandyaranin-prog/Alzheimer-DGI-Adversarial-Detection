# Alzheimer MRI – Adversarial Attack Detection Using Deep Graph Infomax

## Research Overview

This repository contains the Python implementation of a research framework for adversarial attack detection and severity estimation in deep learning-based Alzheimer’s MRI classification.

The proposed framework investigates the use of Convolutional Neural Networks (CNNs), Graph Convolutional Networks (GCNs), and Deep Graph Infomax (DGI) for learning image representations and identifying adversarial perturbations.

## Research Objectives

- Extract meaningful features from Alzheimer’s MRI images using CNNs.
- Construct a similarity graph using cosine similarity.
- Learn graph representations using GCN and Deep Graph Infomax.
- Generate adversarial examples using FGSM, PGD, and Carlini–Wagner attacks.
- Detect adversarial inputs and estimate perturbation severity.
- Evaluate the framework using standard classification and detection metrics.

## Dataset

The implementation uses the Alzheimer MRI dataset containing 6,400 images across four diagnostic categories:

- Non-Demented
- Very Mild Demented
- Mild Demented
- Moderate Demented

Dataset source: [Mendeley Data](https://data.mendeley.com/datasets/3r8hw8wmmk/1)

DOI: 10.17632/3r8hw8wmmk.1

The dataset is not included in this repository. Users should obtain it from the original source and follow its licence conditions.

## Implementation Progress

| Stage | Description | Status |
|---|---|---|
| 1 | Dataset Audit | Completed |
| 2 | Image Validation | Completed |
| 3 | Preprocessing and Data Splitting | Pending |
| 4 | CNN Feature Extraction | Pending |
| 5 | Graph Construction | Pending |
| 6 | Graph Convolutional Network | Pending |
| 7 | Deep Graph Infomax | Pending |
| 8 | Adversarial Attack Generation | Pending |
| 9 | Attack Detection and Severity Estimation | Pending |
| 10 | Evaluation and Results | Pending |

## Technologies

- Python
- Google Colab
- PyTorch
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

## Repository Structure

The implementation notebooks will be organised by research stage.

## Research Status

This repository is under active development. Implementation details, experimental results, figures, and evaluation outputs will be updated as the research progresses.

## Citation

Research manuscript:

"An Unsupervised Graph-Based Framework for Adversarial Attack Detection and Severity Estimation in Deep Learning-Based Alzheimer’s MRI Classification."

Full citation details will be added after publication.
