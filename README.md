# Graph Neural Network-Based Multi-Label Classification of Breast Cancer Using Multiparametric MRI and Clinical Features

## Overview
This repository contains the implementation of a Graph Neural Network (GNN) framework for multi-label classification of breast cancer using multiparametric MRI and clinical features. The model integrates radiomic and clinical data into a unified volumetric graph representation and employs Graph Isomorphism Networks (GIN) to predict key diagnostic parameters, including HER2 status, tumor staging (TNM), and histological grading components.

## Key Features
- **Volumetric Graph Construction**: Converts 3D MRI scans into graph structures where nodes represent voxels and edges capture spatial/intensity relationships.
- **Multi-Label Classification**: Simultaneously predicts HER2 status, TNM staging (Tumor Size, Node Involvement, Metastasis), and tumor grade components (Tubule formation, Mitotic count, Nuclear pleomorphism).
- **Graph Isomorphism Network (GIN)**: Uses GINConv layers for effective graph representation learning.
- **Class Imbalance Handling**: Implements SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalance.
- **Comprehensive Evaluation**: 5-fold cross-validation with metrics including accuracy, precision, recall, F1-score, and confusion matrices.

## Dataset
The Duke Breast Cancer MRI Dataset is used, which includes:
- 922 biopsy-confirmed cases of invasive breast cancer.
- Five MRI modalities: T1-weighted (ax-T1), three phases of post-contrast dynamic sequences (ph1ax-3D-dyn, ph2ax-3D-dyn, ph3ax-3D-dyn), and a fused modality (IHS-Fused).
- Clinical metadata and expert-annotated segmentations.
