
# An Unsupervised Graph-Based Anomaly Detection Framework for Adversarial Perturbations in Deep Learning-Based Alzheimer’s MRI Classification

## Overview

This repository contains the experimental implementation of an unsupervised graph-based anomaly detection framework for identifying adversarial perturbations in deep learning-based Alzheimer’s MRI classification.

The framework combines Convolutional Neural Networks (CNNs), graph construction and Deep Graph Infomax (DGI) with Graph Convolutional Networks (GCNs) to learn image representations and investigate anomalous patterns caused by adversarial perturbations.

The study evaluates three unsupervised anomaly detection methods against three adversarial attack techniques.

## Research Objectives

The main objectives of this research are:

- To extract deep feature representations from Alzheimer’s MRI images using a CNN.
- To construct a cosine-similarity k-nearest-neighbour (kNN) graph from the extracted image embeddings.
- To learn graph-based representations using Deep Graph Infomax and Graph Convolutional Networks.
- To investigate adversarial perturbations generated using FGSM, PGD and CW-L2 attacks.
- To evaluate unsupervised anomaly detection methods using validation-based threshold calibration.
- To assess detection performance using matched clean–adversarial pairs and full test-set evaluation.

## Dataset

The experiments use the Alzheimer MRI dataset containing 6,400 images distributed across four diagnostic categories:

- Mild Demented: 896 images
- Moderate Demented: 64 images
- Non-Demented: 3,200 images
- Very Mild Demented: 2,240 images

**Dataset source:**  
https://doi.org/10.17632/3r8hw8wmmk.1

The images are processed as 128 × 128 grayscale inputs. The dataset is divided into training, validation and testing subsets using a stratified image-level split.

## Methodology

The proposed experimental framework consists of the following major components:

1. Dataset auditing and image validation.
2. Image preprocessing and data splitting.
3. CNN-based feature extraction.
4. Cosine-similarity kNN graph construction.
5. Deep Graph Infomax representation learning using GCNs.
6. Adversarial attack generation.
7. Graph-based anomaly detection.
8. Anomaly scoring and evaluation.
9. Validation-based threshold calibration.
10. Threshold sensitivity analysis and final evaluation.

### Adversarial Attacks

The following adversarial attack methods are investigated:

- Fast Gradient Sign Method (FGSM)
- Projected Gradient Descent (PGD)
- Carlini–Wagner L2 (CW-L2)

### Unsupervised Anomaly Detection Methods

Three anomaly scoring approaches are evaluated:

- k-Nearest-Neighbour (kNN) distance
- Regularised Mahalanobis distance
- Local affinity anomaly score

Detection thresholds are calibrated using the 95th percentile of clean validation scores.

## Experimental Notebooks

The Jupyter/Google Colab notebooks are organised by experimental stage.

| Stage | Description |
|---|---|
| Stage 1 | Dataset audit |
| Stage 2 | Image validation |
| Stage 3 | Preprocessing and data splitting |
| Stage 4 | CNN feature extraction |
| Stage 5 | Graph construction |
| Stage 6 | DGI-GCN implementation |
| Stage 7 | Adversarial attack generation and corrected attack experiments |
| Stage 8 | DGI-GCN adversarial detection experiments, including diagnostic and corrected variants |
| Stage 9 | Threshold calibration and severity-related experiments |
| Stage 10 | Threshold sensitivity and final evaluation |
| Stage 11 | CW-L2 detection enhancement investigation |
| Stage 12 | Final graph-based anomaly detection experiments, including leakage-controlled and paired-evaluation variants |

Additional notebooks labelled A, B and C represent intermediate, diagnostic or refined experimental versions where applicable. They are retained to document the development and evaluation of the research methodology.

**Important:** The final results reported in the manuscript should be associated with the corresponding corrected final experimental notebooks, rather than exploratory or diagnostic versions.

## Evaluation Strategy

The framework is evaluated using two complementary protocols:

1. **Paired evaluation:** Each successful adversarial test sample is compared with its corresponding clean test sample.
2. **Full test-set evaluation:** Successful adversarial samples are evaluated alongside the complete clean test set.

The evaluation considers:

- Precision
- Recall
- F1-score
- False Positive Rate (FPR)
- Receiver Operating Characteristic – Area Under the Curve (ROC-AUC)

The experimental analysis also includes checks for embedding consistency and information leakage in the anomaly detection evaluation.

## Key Experimental Findings

The paired evaluation included 793 successful adversarial samples for each attack.

The local affinity anomaly score achieved its strongest reported result against CW-L2 attacks:

- ROC-AUC: 0.8546
- Precision: 0.8372
- Recall: 0.1362
- F1-score: 0.2343

Detection performance varied across attack methods and scoring approaches. In particular, detection of FGSM and PGD perturbations remained limited at the calibrated thresholds.

These findings highlight the attack-dependent behaviour of unsupervised graph-based anomaly detection.

## Repository Structure

```text
Alzheimer-DGI-Adversarial-Detection/
│
├── README.md
│
├── Stage1- Dataset Audit.ipynb
├── Stage2 - Image Validation.ipynb
├── Stage3 - Preprocessing and Data Splitting.ipynb
├── Stage4 - CNN Feature Extraction.ipynb
├── Stage5 - Graph Construction.ipynb
├── Stage6 - DGI GCN Implementation.ipynb
├── Stage7 - Adversarial Attack Generation Experiments.ipynb
├── Stage7 - Final Corrected Adversarial Attacks.ipynb
├── Stage8 - DGI GCN Adversarial Detection.ipynb
├── Stage8A - Embedding Centroid Diagnostic.ipynb
├── Stage8 - Corrected DGI GCN Adversarial Detection.ipynb
├── Stage9 - Threshold Calibration and Severity.ipynb
├── Stage10 - Threshold Sensitivity and Final Evaluation.ipynb
├── Stage11 - CW-L2 Detection Enhancement Investigation.ipynb
├── Stage12 - Experimental Notebooks.ipynb
├── Stage12B - Leakage Controlled Unsupervised Detection.ipynb
└── Stage12C - Final Train-Only Paired Evaluation.ipynb
```

*The structure above is a guide to the experimental stages. The actual filenames in the repository may differ.*

## Reproducibility

The notebooks are provided to document the experimental workflow and support reproducibility of the research.

To reproduce the experiments:

1. Open the required notebook in Google Colab or Jupyter Notebook.
2. Install the required Python dependencies.
3. Obtain the dataset from the source specified above.
4. Configure the dataset paths and experiment parameters.
5. Execute the notebooks in the appropriate experimental order.
6. Refer to the final corrected notebooks for the experiments corresponding to the manuscript results.

The notebook execution environment, dependency versions, random seeds and model checkpoints should be maintained consistently when reproducing the reported results.

## Technologies Used

- Python
- Google Colab
- Jupyter Notebook
- PyTorch
- PyTorch Geometric / Graph Neural Network components
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

## Research Status

This repository accompanies a research manuscript titled:

**An Unsupervised Graph-Based Anomaly Detection Framework for Adversarial Perturbations in Deep Learning-Based Alzheimer’s MRI Classification**

The repository documents the experimental development, implementation and evaluation of the proposed framework.

## Author

**Dr. N. Sandya Rani**

Researcher – Computer Science and Engineering  
Research Area: Artificial Intelligence, Adversarial Machine Learning, Graph Neural Networks and Medical Image Analysis

## Citation

If you use this repository or build upon this research, please cite the associated research publication once it is published.

---

**Note:** This repository is intended for academic research and experimentation. The proposed framework is a research investigation and is not intended for direct clinical diagnosis or deployment.
```

The README above reflects the title and findings in your latest manuscript. <FileCite ref_id="turn58file0" />
