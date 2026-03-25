# SDDF: Specificity-Driven Dynamic Focusing for Open-Vocabulary Camouflaged Object Detection (CVPR 2026)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Paper](https://img.shields.io/badge/Paper-ArXiv-red.svg)](#) [![Venue: CVPR 2026](https://img.shields.io/badge/Venue-CVPR_2026-blue.svg)](#)

> **🚧 Update (2026):** Our paper has been accepted by CVPR 2026! **The code and dataset (OVCOD-D) are coming soon. Please stay tuned!** ## 📖 Introduction

Open-vocabulary object detection (OVOD) has demonstrated strong zero-shot generalization capabilities. However, when dealing with **camouflaged objects**, detectors often fail to distinguish and localize targets because their visual features are highly similar to the background. 

To bridge this gap, we construct a new benchmark named **OVCOD-D** and propose **SDDF** (Specificity-Driven Dynamic Focusing). Our method addresses the two main challenges in open-vocabulary camouflaged object detection:
1. **Noisy Textual Embeddings:** We design a sub-description principal component contrastive fusion strategy (using SVD) to filter out confusing and overly decorative modifiers.
2. **Highly Similar Visual Embeddings:** We propose a specificity-guided regional weak alignment and dynamic focusing method (SF-GLU module) to strengthen the detector's ability to discriminate camouflaged objects from the background.

Under the open-set evaluation setting, **SDDF achieves a State-of-the-Art AP of 56.4 on the OVCOD-D benchmark.**

## ⚙️ Architecture

![SDDF Framework](assets/framework.png)
*Figure: Overall architecture of the proposed specificity-driven open-vocabulary camouflaged object detector. Fine-grained textual sub-descriptions are decorrelated via SVD, refined, and integrated with visual object embeddings.*

## 🏆 Main Results

### Comparison with SOTA COD Methods
We compare SDDF with other State-of-the-Art Camouflaged Object Detection methods on the OVCOD-D dataset. Our model demonstrates superior localization capabilities:

| Method | Backbone | AP | AP$_{50}$ | AP$_{75}$ |
| :--- | :---: | :---: | :---: | :---: |
| SINet-V2 | ResNet-50 | 40.2 | 69.3 | 39.4 |
| FSPNet | Swin-T | 47.9 | 76.2 | 49.4 |
| CamoFormer | Swin-T | 55.6 | 80.2 | 59.0 |
| HDPNet | ViT-B | 56.3 | **81.5** | 59.6 |
| **SDDF-L (Ours)** | **YOLOv8-L** | **56.4** | 76.4 | **60.7** |

### Qualitative Performance
![Qualitative Results](assets/qualitative.png)
*Figure: Visualization of detection bounding boxes and heatmap representations of the response differences with our proposed SF-GLU module.*

## 📧 Contact
If you have any questions, please feel free to contact us or open an issue.
