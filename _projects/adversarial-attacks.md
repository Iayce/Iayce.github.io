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

### SEASON (Cross-Architecture Transfer Enhancement)
- **Hybrid Noise Strategy**: Combined gradient perturbation with salt-pepper noise
- **Transfer Improvement**: Enhanced cross-architecture transfer success rate by 3.6%
- **Visual Quality**: Optimized perturbation focus by 37% while maintaining industry-leading visual quality

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
- **ICCV 2025**: Three first-author papers submitted, with FastJSMA accepted (434→544 score)
- **Publications**: Watertox paper published in arXiv (2024) - [View Publication](/publications/#gao2024watertoxartsimplicityuniversal)
- **Industry Application**: Methods applicable to model security and robustness testing

## Key Contributions

### Technical Leadership
- **Algorithm Design**: Led core algorithm development and experimental validation
- **Cross-Method Optimization**: Coordinated multiple attack strategies for enhanced performance
- **Comprehensive Testing**: Covered multiple datasets and model architectures

### Research Output
- **Publications**: Three ICCV 2025 submissions as co-first author
- **Performance**: Achieved state-of-the-art results in attack efficiency and transferability
- **Practical Impact**: Developed methods with real-world security applications

---

