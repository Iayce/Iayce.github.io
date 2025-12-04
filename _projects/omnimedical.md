---
layout: page
title: "OmniMedical: Multi-Agent Explainable Drug Discovery Platform"
description: An end-to-end, multi-agent and explainable AI platform for small-molecule drug discovery and intelligent delivery
img: assets/img/Project/OmniMedical/OmnMedical_1031_v2_06.png
importance: 2
category: research
published: true
---

## Project Overview

**OmniMedical** is an end-to-end **multi-agent explainable drug discovery platform** that covers the full pipeline from target-centric molecular generation and virtual screening to lead optimization and intelligent delivery design.  
The system is designed as a rigorous AI-for-drug-discovery research platform rather than a demo or competition project.

### Demo Video

<video controls class="img-fluid rounded z-depth-1 mb-3" style="max-width: 800px; width: 100%;">
  <source src="/assets/video/OmniMedical.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<p>
  If the embedded player cannot load properly, you can
  <a href="/assets/video/OmniMedical.mp4" target="_blank">open / download the video file directly</a>.
</p>

### System Architecture Figure

<img src="/assets/img/Project/OmniMedical/OmnMedical_1031_v2_06.png"
     alt="OmniMedical System Architecture"
     class="img-fluid rounded z-depth-1 mb-4">

---

## Research Motivation

Current small-molecule drug discovery pipelines suffer from high experimental cost, long development cycles and fragmented tooling. In particular:

- Conventional virtual screening pipelines are expensive to scale and difficult to interpret.
- Existing AI models often focus on isolated stages (e.g., generation or docking) and rarely provide an **end-to-end** view from target to candidate.
- Delivery design and late-stage optimization are typically decoupled from early-stage molecular design.

OmniMedical aims to provide a **single, modular research platform** that integrates these stages into an explainable, multi-agent workflow.

---

## System Design

OmniMedical is organized into three conceptual layers:

1. **Data & Knowledge Layer**  
   - Curated disease–target databases, molecular libraries and biomedical knowledge graphs.
2. **Algorithm & Agent Layer**  
   - Task-specific agents for molecular generation, drug repurposing, virtual screening, evaluation and delivery design.
   - Coordination mechanisms that combine large language models with graph neural networks and physics-inspired models.
3. **Application Layer**  
   - Web-based interface for interactive analysis, visualization and experiment management.

---

## Core Modules

### 1. Target-aware Multimodal Molecular Generation

- Uses both **3D target structures** and **protein sequences** as conditioning signals.
- Structure branch: TamGen-style structure-guided generator for pocket-specific ligand design.
- Sequence branch: reinforcement learning–enhanced large language model for SMILES/graph generation.
- Cross-consistency constraints encourage candidates that are simultaneously structure-compatible and chemically feasible.

### 2. Knowledge-graph-driven Drug Repurposing

- Large-scale biomedical knowledge graph connecting diseases, targets, drugs and pathways.
- Multi-agent reasoning framework:
  - Graph reasoning agent proposes candidate disease–target–drug triples.
  - Mechanism analysis agent aggregates literature and pathway evidence.
  - Safety agent filters candidates using side-effect and pharmacokinetic profiles.

### 3. Three-stage Virtual Screening Pipeline

1. **GNN-based Primary Screening**  
   - Uses **DumplingGNN** to score large molecular libraries based on physicochemical properties, ADMET profiles and toxicity surrogates.
2. **Deep-learning-based Docking and Scoring**  
   - Applies a Boltz2-style deep docking model to predict binding poses and affinity for top-ranked molecules.
3. **Pose Refinement and BioScore Aggregation**  
   - Refines poses and computes a BioScore-derived composite score, yielding an interpretable ranking.

### 4. Multi-dimensional Evaluation and Explainability

- Multi-criteria scoring across potency, ADMET, toxicity and developability.
- Attention and attribution techniques provide **substructure-level explanations** for model decisions.
- Full traceability from final score back to individual module contributions.

### 5. Lead Optimization and Delivery Design

- Retrieval-augmented reinforcement learning loop for iterative lead optimization.
- Automatic proposal of delivery strategies (e.g., formulation and route hints) with structured reports for downstream experimental design.

---

## Experimental Evaluation

- Benchmarked on multiple public ADMET and property-prediction datasets, where individual components of OmniMedical achieve competitive or state-of-the-art performance.
- End-to-end studies show that the integrated pipeline outperforms conventional docking-centric workflows in both screening efficiency and hit quality, while providing richer interpretability.

---

## Relation to Other Work

OmniMedical is conceptually related to recent multimodal and cross-architecture frameworks (e.g., DrugCLIP-like systems), but emphasizes:

- **Explicit multi-agent decomposition** of the drug discovery pipeline.
- Tight integration of **GNNs, deep docking models and LLM-based agents**.
- End-to-end **explainability** across generation, screening and delivery stages.
