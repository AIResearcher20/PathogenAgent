# 🧬 PathogenAgent

![Agentic AI](https://img.shields.io/badge/Agentic_AI-Medical_Reasoning-blue)
![Genomics](https://img.shields.io/badge/Genomics-Variant_Interpretation-red)
![RAG System](https://img.shields.io/badge/RAG-Evidence_Based-orange)
![LLM](https://img.shields.io/badge/BioGPT-Fine_Tuned-green)
![Status](https://img.shields.io/badge/Status-Research_Project-purple)
---

---

## 📌 Overview

PathogenAgent is an agentic artificial intelligence system designed for clinical variant interpretation in genomic medicine.

The system combines biomedical knowledge retrieval, multi-step reasoning, and large language model generation to produce evidence-grounded interpretations of genetic variants.

It integrates structured data sources such as:

- ClinVar (NCBI)
- PubMed
- GenBank

into a modular AI pipeline for biomedical reasoning and analysis.

---

## 🧠 System Architecture

![Architecture](assets/pathogenagent_architecture.png)

The system is composed of two main subsystems:

---

## 🧬 1. Dataset Engineering Pipeline (8 Modules)

This pipeline processes raw ClinVar data (~2,000,000 variants) into structured datasets suitable for analysis and model usage.

Modules:

1. Data Acquisition (ClinVar parsing and loading)
2. Data Cleaning (missing values, normalization)
3. Feature Engineering (gene, chromosome, variant features)
4. BioGPT-Compatible Formatting
5. Statistical Analysis
6. Data Visualization
7. Dataset Splitting (Train / Validation / Test)
8. Final Dataset Preparation

---

## 🤖 2. PathogenAgent Reasoning System (10 Modules)

This subsystem performs end-to-end biomedical question answering and variant interpretation.

Modules:

1. Intent Router (query classification)
2. Tool Executor (PubMed / ClinVar / GenBank retrieval)
3. Evidence Integration (multi-source aggregation)
4. Evidence Ranking (semantic + statistical ranking)
5. Retrieval-Augmented Generation (RAG pipeline)
6. Reflection Agent (self-evaluation of reasoning quality)
7. BioGPT Generator (response generation module)
8. Verification Agent (hallucination detection & factual consistency)
9. Report & Logger (structured output generation)
10. Orchestrator (pipeline coordination)

---

## 🧬 Language Model

A previously fine-tuned BioGPT model is used as the core generation component of the system:

- Model: https://huggingface.co/Sepideh2027/biogpt-clinvar-finetuned  
- Architecture: BioGPT (Causal Language Model)  
- Training Data: ClinVar variant dataset  
- Domain: Clinical variant interpretation

This model is integrated as Module 7 (BioGPT Generator) within the agentic pipeline.

---

## 📊 Dataset

- Source: ClinVar (NCBI)
- Scale: ~2,000,000 genetic variants
- Features:
  - Gene symbol
  - Chromosome
  - Variant type
  - Clinical significance

Data processing includes:

- Cleaning and normalization
- Feature selection
- Gene-wise structuring
- Train/validation/test splitting

---

## 🛠 Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-yellow?style=for-the-badge)
![FAISS](https://img.shields.io/badge/FAISS-blue?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-orange?style=for-the-badge)

---

## 📈 Current Implementation Status

### 🧬 Dataset Pipeline
✔ Data acquisition completed  
✔ Data cleaning completed  
✔ Feature engineering completed  
✔ Data visualization completed  
✔ Dataset splitting completed  

---

### 🤖 PathogenAgent System
✔ Modular architecture designed  
✔ Initial system integration completed  

🚧 In Progress:
- Retrieval-Augmented Generation (RAG) optimization
- Reflection module improvement
- Verification module tuning
- End-to-end evaluation pipeline
- LoRA fine-tuning experiments

---

## 🔬 Key Contributions

- Design of a dual-system architecture separating dataset engineering and reasoning components
- Development of an agentic AI framework for biomedical question answering
- Integration of retrieval-based biomedical knowledge sources with LLM reasoning
- Application of BioGPT for domain-specific genomic interpretation
- Implementation of verification mechanisms for hallucination reduction
- Modular system design suitable for extension and research

---

## 📦 Installation

```bash
pip install -r requirements.txt


---

🚀 Project Status

This project is an ongoing research effort in biomedical artificial intelligence and genomic reasoning.

It focuses on building reliable, evidence-based AI systems for clinical variant interpretation using agentic architectures.


---

📂 Related Work

A previous prototype system and fine-tuned BioGPT model were developed independently and are publicly available.

This project extends that work into a full agentic AI framework.


---

📄 License

MIT License


---

👤 Author

وانیا کریمی 

---

# 🧠 
