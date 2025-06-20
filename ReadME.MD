# VERITAS: Verification and Explanation of Realness in Images for Transparency in AI Systems

## Abstract

The widespread adoption of AI-generated content has revolutionized the digital media landscape, enabling efficient and creative content generation while simultaneously raising concerns regarding content authenticity and integrity. While many existing solutions focus solely on classification, they often lack transparency in their decision-making. In this paper, we present VERITAS, a comprehensive framework that not only accurately detects whether an image is AI-generated but also explains why it was classified that way through artifact localization and semantic reasoning. Our architecture couples traditional image classifiers with a novel interpretability pipeline that employs GradCAM, patch-wise weighting, CLIP-based scoring, and a multimodal language model (MOLMO) to produce human-readable explanations of detected artifacts. We show that this architecture is robust to adversarial attacks and propose ablation studies across various vision-language models (VLMs), culminating in our selection of MOLMO for its semantic coherence and precision.

## Features
- **Artifact Detection and Explainability**: Utilizes advanced interpretability techniques to highlight and analyze distinguishing features.
- **Super-Resolution for Detailed Analysis**: Applies super-resolution techniques to improve artifact detection in case of low-resolution images.

## Methodology
### 1. Classification Experiments Framework
- Utilizes an ensemble of EfficientNet, ResNet-18, and ViT-Tiny for robust classification.
- Trained on an augmented CIFAKE dataset, incorporating adversarially modified images.
- Implements a weighted ensemble approach to optimize predictive performance.

### 2. Artifact Detection Mechanism
- Enhances image resolution using DRCT (Diffusion Reconstruction Contrastive Training) Super-Resolution models.
- Applies GradCAM-based heatmaps to visualize decision-critical regions.
- Utilizes CLIP-based scoring to quantify and rank unnatural features.
- Leverages MOLMO to generate textual descriptions of detected artifacts, improving interpretability.

## Pipelines
### 1. Classification Framework Pipeline
![Task 1 pipeline](pipeline_structures/Task_1_pipeline_structure.png?raw=true "Task 1 Pipeline")
### 2. VERITAS pipeline
![Task 2 pipeline](pipeline_structures/Task_2_pipeline_structure.png?raw=true "Task 2 Pipeline")

## Dataset Composition for the Classification Experiments
The dataset builds upon the CIFAKE dataset, integrating adversarial perturbations from:
- **Fast Gradient Sign Method (FGSM)**: Introduces minimal perturbations to deceive classifiers.
- **Projected Gradient Descent (PGD)**: Iteratively refines perturbations for enhanced evasion.
- **AutoAttack**: Employs an ensemble of adversarial attack strategies.
- **AuraSR**: Includes images generated via GAN-based techniques to improve dataset diversity.

## Model Performance
| Model               | Accuracy (%) |
|---------------------|-------------|
| EfficientNet        | 87.7        |
| ResNet-18          | 83.5        |
| ViT-Tiny           | 83.1        |
| **Ensemble Model** | **93.1**    |


