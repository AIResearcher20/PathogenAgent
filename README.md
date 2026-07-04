<div align="center">

# 🧬 PathogenAgent  

![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![BioGPT](https://img.shields.io/badge/BioGPT-Fine--Tuned-9C27B0?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-Enabled-orange?style=for-the-badge)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20Search-blue?style=for-the-badge)
![Dataset](https://img.shields.io/badge/ClinVar-2M%20Variants-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

---

### 🧠 Agentic AI System for Evidence-Based Genomic Variant Interpretation  
### 🔬 Retrieval-Augmented Biomedical Reasoning with Multi-Agent Architecture  
### 🤖 Fine-Tuned BioGPT + ClinVar + PubMed + GenBank Integration  

</div>
---
# 🧬 PathogenAgent

### 🧬 Agentic AI System for Clinical Variant Interpretation: Retrieval-Augmented Biomedical Reasoning with Fine-Tuned Language Models

---

## 📌 Overview

**PathogenAgent** is an agentic artificial intelligence system designed for clinical variant interpretation in genomic medicine.

The system integrates large-scale genomic data processing, multi-source biomedical retrieval, and multi-step reasoning to generate evidence-grounded interpretations of genetic variants.

The framework combines structured biomedical resources including:

- ClinVar (NCBI)
- PubMed
- GenBank

within a modular AI architecture for biomedical reasoning and analysis.

---

## 🧠 System Architecture

![Architecture](assets/pathogenagent_architecture.png)

The proposed system consists of two interconnected subsystems:

- Dataset Engineering Pipeline (8 modules)
- Agentic Reasoning Framework (10 modules)

---

# 📊 Part I: Dataset Engineering Pipeline

## 1.1 Dataset Overview

The system processes a large-scale ClinVar dataset containing **8,991,566 genetic variants** with **10 structured features**.

| Property | Value |
|----------|------|
| Total Variants | 8,991,566 |
| Features | 10 |
| Unique Genes | 500+ |
| Clinical Classes | 4 |
| Source | ClinVar (NCBI) |

---

## 1.2 Clinical Significance Distribution

| Class | Percentage | Count |
|------|------------|------|
| Likely Benign | 67.03% | 6,027,000+ |
| Benign | 13.06% | 1,174,000+ |
| Pathogenic | 12.45% | 1,119,000+ |
| Likely Pathogenic | 7.46% | 671,000+ |

---

## 1.3 Top Genes by Variant Frequency

| Gene | Approx. Count |
|------|--------------|
| BRCA2 | ~40,000 |
| NF1 | ~35,000 |
| BRCA1 | ~30,000 |
| NEB | ~28,000 |
| ATM | ~25,000 |
| DMD | ~22,000 |
| USH2A | ~20,000 |
| FBN1 | ~18,000 |
| RYR1 | ~15,000 |
| APC | ~12,000 |

---

## 1.4 Chromosomal Distribution

The distribution of variants shows high concentration across major chromosomes, with chromosome 1–5 carrying the highest variant loads.

---

## 1.5 Dataset Processing Pipeline (8 Modules)

1. Data Acquisition (ClinVar parsing from NCBI)
2. Data Cleaning (missing values, normalization, deduplication)
3. Feature Engineering (gene, chromosome, variant features)
4. Statistical Analysis
5. Data Visualization
6. BioGPT-Compatible Formatting
7. Dataset Splitting (Train / Validation / Test)
8. Final Dataset Preparation

---

# 🧬 Part II: Agentic AI Architecture

## 2.1 Core Language Model

A previously fine-tuned BioGPT model is used as the core generation component:

- Model: Sepideh2027/biogpt-clinvar-finetuned  
- Architecture: BioGPT (Causal Language Model)  
- Domain: Clinical variant interpretation  
- Platform: Hugging Face Hub  

---

## 2.2 Agentic Reasoning Pipeline (10 Modules)

The system implements a modular agent-based reasoning architecture:

### 1. Intent Router
Query classification and routing to appropriate tools.

### 2. Tool Executor
Biomedical retrieval from PubMed, ClinVar, GenBank.

### 3. Evidence Integration
Normalization and merging of multi-source evidence.

### 4. Evidence Ranking
Semantic + statistical ranking of retrieved evidence.

### 5. RAG Context Builder
Construction of retrieval-augmented context.

### 6. Reflection Agent
Evaluation of evidence quality and completeness.

### 7. BioGPT Generator
Fine-tuned model for clinical interpretation generation.

### 8. Verification Agent
Detection of hallucinations and factual inconsistencies.

### 9. Report & Logger
Structured output generation (JSON / Markdown / PDF).

### 10. Orchestrator
End-to-end pipeline coordination and execution.

---

## 2.3 System Flow

User Query  
↓  
Intent Router  
↓  
Tool Executor (PubMed / ClinVar / GenBank)  
↓  
Evidence Integration  
↓  
Evidence Ranking  
↓  
RAG Context Builder  
↓  
Reflection Agent  
↓  
BioGPT Generator  
↓  
Verification Agent  
↓  
Report & Logger  
↓  
Orchestrator → Final AgentResult  

---

## 📊 Dataset–Model Integration

| Component | Role |
|----------|------|
| Dataset Pipeline | Data processing and structuring |
| Agentic Pipeline | Inference and reasoning |
| BioGPT Model | Language generation backbone |
| Shared Artifacts | Gene/variant mappings |

---

## 🔬 Key Contributions

- Large-scale ClinVar dataset engineering (8.9M variants)
- Modular 8-stage dataset processing pipeline
- 10-module agentic biomedical reasoning framework
- Integration of retrieval, reasoning, and generation components
- Fine-tuned BioGPT for clinical variant interpretation
- Verification layer for hallucination reduction

---

## 🛠 Tech Stack

**Core:**
- PyTorch
- Hugging Face Transformers
- Sentence Transformers
- FAISS

**Data:**
- Pandas
- NumPy
- Scikit-learn
- SciPy

**Biomedical APIs:**
- NCBI Entrez (PubMed, ClinVar, GenBank)

---

## 📈 Project Status

### Dataset Pipeline
✔ Data acquisition completed  
✔ Data cleaning completed  
✔ Feature engineering completed  
✔ Dataset structuring completed  
✔ Train/validation splitting completed  

### Agentic System
✔ Modular architecture designed  
✔ Initial system integration completed  

🚧 In Progress:
- RAG optimization
- Reflection module tuning
- Verification module improvement
- End-to-end evaluation pipeline
- Manuscript preparation

---

## 📦 Installation

```bash
git clone https://github.com/yourusername/PathogenAgent.git
cd PathogenAgent
pip install -r requirements.txt


---

📄 License

MIT License


---

👤 Author

Vania Karimi


---

📎 Related Work

BioGPT Model: Sepideh2027/biogpt-clinvar-finetuned

ClinVar Dataset: Sepideh2027/clinvar-project-backup



---

📧 Contact

For collaboration or questions, please open an issue in this repository.


---

🙏 Acknowledgments

NCBI for ClinVar, PubMed, GenBank

Hugging Face for infrastructure

BioGPT research community


---

