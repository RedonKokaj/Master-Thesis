# Master Thesis

## Overview

This repository contains the **presentation (PDF)** of my Master’s Thesis titled:

**“Leveraging Large Language Models for Fileless Malware Detection at the Edge.”**

The presentation summarizes the motivation, research questions, methodology, experimental evaluation, and key results of the thesis.

At this stage, **only the presentation is publicly available**. The source code, trained models, and implementation details are intentionally kept private due to academic and institutional constraints.

## Availability of Materials

* 📄 **Presentation**: Available in PDF format in this repository.
* 💻 **Source Code**: Not publicly available at the moment.

The code has been withheld due to academic and/or institutional requirements. It may be released in the future after evaluation, publication, or explicit authorization.

## Thesis Context

* **Degree**: Master’s Degree (MSc) in Computer Science
* **Institution**: University of Insubria
* **Academic Year**: 2024/2025
* **Author**: Redon Kokaj

## Thesis Summary

The thesis addresses the growing threat of **fileless malware**, a class of attacks that operates entirely in memory and abuses legitimate system tools (Living-Off-The-Land), making traditional signature-based antivirus solutions largely ineffective.

The core objective of this work is to **design and validate a lightweight, edge-ready detection system** based on **Large Language Models (LLMs)** that can identify subtle malicious patterns in memory artifacts while operating under strict resource constraints.

The presentation covers:

* The fileless malware threat model and its unique characteristics
* Limitations of traditional detection approaches
* The use of **distilled transformer models** for efficient edge deployment
* Dataset construction and harmonization
* Experimental evaluation under realistic conditions
* Key findings and future research directions

## Methodology Overview

The proposed system follows a modular pipeline:

1. **Data Preparation**: Memory artifacts extracted using the Volatility framework and harmonized across multiple datasets.
2. **Model Selection**: Comparison between two distilled transformer architectures:
   * **DistilBERT** (encoder-only, bidirectional)
   * **DistilGPT-2** (decoder-only, autoregressive)
3. **Knowledge Distillation**: Leveraging large teacher models to transfer knowledge to compact student models.
4. **Fine-Tuning**: Supervised training for binary malware detection.
5. **Edge-Oriented Deployment**: Focus on low latency and efficiency.

## Experimental Evaluation

The models were evaluated through a comprehensive experimental campaign including:

* Comparison against classical baselines (Random Forest, KNN)
* Robust validation strategies (**KFold vs GroupKFold**) to avoid data leakage
* **Few-shot and zero-shot learning** scenarios to assess data scarcity resilience
* **Class imbalance testing** with varying benign/malicious ratios
* **Cross-dataset generalization** to unseen environments

Key findings highlight that GroupKFold validation provides a more realistic estimate of performance, and that **DistilBERT demonstrates superior stability and generalization**, while **DistilGPT-2 achieves higher peak performance in specific scenarios**.
