---
layout: page
title: Adversarial Attack Optimization & Cross-Architecture Robustness
description: Multi-dimensional optimization framework for efficient adversarial attacks
img: assets/img/Project/FastJSMA.png
importance: 4
category: research
related_publications: true
published: true
---

## Project Overview

Developed a multi-dimensional optimization framework for adversarial attacks, integrating gradient decoupling, hybrid noise strategies, and model ensemble approaches to improve attack efficiency and cross-architecture transferability.

## Core Algorithms

### FastJSMA (Fast Jacobian-based Saliency Map Attack)
- **Gradient Decoupling**: Optimized traditional JSMA complexity to 1/80 of original method
- **Performance**: Achieved 81x speedup on CIFAR-100 while maintaining 98%+ success rate
- **Scalability**: First method to support ImageNet large-scale attacks, breaking memory limitations

### Season (Spectrum-Aware Orthogonal Gradient Refinement)
- **Spectrum-aware decoupling**: Gaussian-smoothed low-frequency vs. high-frequency surrogate-gradient branches for structure vs. texture
- **Low-saliency guidance**: Precomputed saliency on the clean image; steers high-frequency updates toward background while preserving foreground shape cues for ViT-like targets
- **Orthogonal refinement**: Projects accumulated high-frequency perturbation onto the orthogonal complement of the low-frequency structural component to reduce branch interference
- **Results**: Training-free wrapper over standard transfer attacks; on ImageNet (ResNet-50 surrogate, unified protocol) average transfer success gains of **+6.6** percentage points (up to **+16.0**) across CNN, ViT, and MLP targets vs.\ strong baselines
- **Venue**: **ICME 2026** (IEEE International Conference on Multimedia and Expo, **CCF-B**), accepted **March 17, 2026**; **Shengjie Xu**, corresponding author — [publication entry](/publications/#wang2026season)

### Watertox (Lightweight Universal Attack Framework)
- **Two-stage FGSM**: Implemented multi-model ensemble with gradient voting
- **Efficiency**: Achieved 1 image/second processing speed
- **Performance**: Reduced target model accuracy by up to 98.8% in zero-shot attacks
- **Competitive Edge**: Outperformed contemporary methods by 3%-5%

## Technical Achievements

### Algorithm Innovation
- **Efficiency Breakthrough**: Solved efficiency and compatibility bottlenecks in large-scale scenarios
- **Cross-Architecture Support**: Successfully tested on 20+ model architectures
- **Dataset Coverage**: Comprehensive evaluation on CIFAR, ImageNet, and other major datasets

### Research Impact
- **ICCV 2025**: FastJSMA accepted (co-first author); presented in Honolulu
- **ICME 2026**: Season accepted March 17, 2026 (**CCF-B**); corresponding author — [View Publication](/publications/#wang2026season)
- **Publications**: Watertox on arXiv (2024) — [View Publication](/publications/#gao2024watertoxartsimplicityuniversal)
- **Industry Application**: Methods applicable to model security and robustness testing

## Key Contributions

### Technical Leadership
- **Algorithm Design**: Led core algorithm development and experimental validation
- **Cross-Method Optimization**: Coordinated multiple attack strategies for enhanced performance
- **Comprehensive Testing**: Covered multiple datasets and model architectures

### Research Output
- **Publications**: FastJSMA at ICCV 2025 (co-first author); Season at ICME 2026 (corresponding author); Watertox preprint (2024)
- **Performance**: Strong results on attack efficiency (FastJSMA) and cross-architecture transfer (Season)
- **Practical Impact**: Methods suitable for security evaluation of heterogeneous vision systems

---

