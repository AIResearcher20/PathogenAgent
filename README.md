PathogenAgent
---
![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![BioGPT](https://img.shields.io/badge/BioGPT-Fine--Tuned-9C27B0?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG-Enabled-orange?style=for-the-badge)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20Search-blue?style=for-the-badge)
![Dataset](https://img.shields.io/badge/ClinVar-2M%20Variants-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge)

---
<p align="center">
  <img src="https://raw.githubusercontent.com/AIResearcher20/REPO/main/assets/logo.png" width="200" />
</p>
---

### 🧠 Agentic AI System for Evidence-Based Genomic Variant Interpretation  
### 🔬 Retrieval-Augmented Biomedical Reasoning with Multi-Agent Architecture  
### 🤖 Fine-Tuned BioGPT + ClinVar + PubMed + GenBank Integration  

</div>
---


### 🧬 Agentic AI System for Clinical Variant Interpretation: Retrieval-Augmented Biomedical Reasoning with Fine-Tuned Language Models

---

📌 Overview

PathogenAgent is an agentic artificial intelligence system for clinical variant interpretation in genomic medicine. The system combines:

Large‑scale genomic data engineering (8.9M ClinVar variants)

Multi‑source biomedical retrieval (PubMed, ClinVar, GenBank)

Evidence‑grounded reasoning via a 10‑module agentic pipeline

Fine‑tuned BioGPT for clinical variant interpretation



---

📊 Part 1: Dataset Engineering

1.1 Dataset Overview

The system processes a comprehensive ClinVar dataset containing 8,991,566 genetic variants with 10 structured features.

Property	Value

Total Variants	8,991,566
Features	10
Unique Genes	500+
Clinical Classes	4
Source	ClinVar (NCBI)


1.2 Clinical Significance Distribution

The dataset captures four primary clinical interpretation classes with the following distribution:

Class	Percentage	Count

Likely Benign	67.03%	6,027,000+
Benign	13.06%	1,174,000+
Pathogenic	12.45%	1,119,000+
Likely Pathogenic	7.46%	671,000+




1.3 Top Genes by Variant Frequency

The most frequently mutated genes in the dataset:

Gene	Variant Count

BRCA2	~40,000
NF1	~35,000
BRCA1	~30,000
NEB	~28,000
ATM	~25,000
DMD	~22,000
USH2A	~20,000
FBN1	~18,000
RYR1	~15,000
APC	~12,000




1.4 Chromosomal Distribution

Variant distribution across chromosomes shows the highest concentration on:

Chromosome	Variant Count

Chromosome 1	~300,000
Chromosome 2	~280,000
Chromosome 3	~260,000
Chromosome 4	~240,000
Chromosome 5	~220,000




1.5 Data Processing Pipeline

The dataset engineering pipeline consists of 8 modular stages:

1. Data Acquisition – Raw ClinVar import from NCBI


2. Data Cleaning – Missing value handling, deduplication, normalization


3. Feature Engineering – Gene, chromosome, position, clinical significance extraction


4. Statistical Analysis – Distribution analysis, class balancing


5. Data Visualization – Exploratory data analysis (EDA)


6. BioGPT‑Compatible Formatting – Text‑to‑text transformation for LLM fine‑tuning


7. Dataset Splitting – Train/Validation/Test (70/15/15)


8. Final Dataset Preparation – Ready for model training and evaluation




---

🧬 Part 2: Model Architecture & Agentic Pipeline

2.1 Core Language Model

The system uses a fine‑tuned BioGPT model as its core reasoning engine:

Property	Value

Model	Sepideh2027/biogpt-clinvar-finetuned
Architecture	BioGPT (Causal Language Model)
Parameters	~300M
Training Data	ClinVar variants (8.9M records)
Domain	Clinical variant interpretation


Model Link: Hugging Face – Sepideh2027/biogpt-clinvar-finetuned

2.2 Agentic Pipeline (10 Modules)

The system implements a 10‑module agentic pipeline for end‑to‑end clinical variant interpretation:

Module 1: Intent Router

Function: Classifies the input query and determines required tools
Input: User query (text)
Output: Intent type + required tools + confidence score

Module 2: Tool Executor

Function: Executes queries across biomedical databases
Sources: PubMed (literature), ClinVar (variants), GenBank (sequences)
Output: Raw evidence from all sources

Module 3: Evidence Integration

Function: Normalizes, deduplicates, and merges evidence
Methods: Identifier‑based deduplication, semantic similarity
Output: Canonical evidence list

Module 4: Evidence Ranking

Function: Scores and ranks evidence by relevance
Methods: TF‑IDF + Semantic Similarity (all‑MiniLM‑L6‑v2) + Cross‑Encoder (optional)
Output: Ranked evidence with composite scores

Module 5: RAG Context Builder

Function: Assembles top‑ranked evidence into structured context
Output: Evidence‑grounded context for LLM generation

Module 6: Reflection Agent

Function: Self‑evaluates reasoning quality and evidence sufficiency
Metrics: Coverage, coherence, confidence calibration
Output: Reflection score + action recommendation

Module 7: BioGPT Generator

Function: Generates evidence‑grounded responses
Model: Sepideh2027/biogpt-clinvar-finetuned
Output: Comprehensive, cited clinical interpretation

Module 8: Verification Agent

Function: Detects hallucinations and verifies factual consistency
Methods: Claim extraction, evidence‑based verification
Output: Faithfulness score + hallucination claims

Module 9: Report & Logger

Function: Generates structured reports and maintains audit logs
Formats: JSON, Markdown, PDF
Output: Complete audit trail

Module 10: Orchestrator

Function: Manages workflow, coordinates module execution
Output: Final structured result (AgentResult)

2.3 Module Interaction Flow

User Query
│
▼
[1. Intent Router] ──► intent, tools
│
▼
[2. Tool Executor] ──► raw evidence
│
▼
[3. Evidence Integration] ──► canonical evidence
│
▼
[4. Evidence Ranking] ──► ranked evidence
│
▼
[5. RAG Context Builder] ──► structured context
│
▼
[6. Reflection Agent] ──► reflection_score
│
▼
[7. BioGPT Generator] ──► generated response
│
▼
[8. Verification Agent] ──► faithfulness_score
│
▼
[9. Report & Logger] ──► JSON / Markdown / PDF
│
▼
[10. Orchestrator] ──► AgentResult


---

📊 Dataset – Model Integration

The 8‑module dataset pipeline and 10‑module agentic pipeline are integrated through:

Component	Role

Dataset Pipeline	Provides training/evaluation data for the model
Agentic Pipeline	Uses the fine‑tuned model for inference
Shared Artifacts	Gene lists, variant classes, clinical significance mappings



---

🔬 Key Contributions

Dataset Engineering

8.9M ClinVar variants processed and structured

10 features extracted per variant

500+ genes with variant annotations

4 clinical significance classes mapped


Model & Architecture

Fine‑tuned BioGPT model publicly available

10‑module agentic pipeline for clinical reasoning

Evidence‑grounded generation with citation tracking

Hallucination detection via verification module



---

🛠 Tech Stack

Core Libraries

PyTorch – Deep learning framework

Transformers (Hugging Face) – Model fine‑tuning

Sentence‑Transformers – Semantic embeddings

FAISS – Vector similarity search


Data Processing

Pandas – Data manipulation

NumPy – Numerical computing

Scikit‑learn – ML utilities


APIs & Services

NCBI Entrez – PubMed, ClinVar, GenBank retrieval

Hugging Face Hub – Model hosting



---

📈 Project Status

✅ Completed

Dataset Engineering: 8.9M ClinVar variants processed (10 features, 500+ genes)

Model Fine‑tuning: BioGPT fine‑tuned on ClinVar (publicly available)

Architecture Design: 10‑module agentic pipeline + 8‑module dataset pipeline

Visualization: Complete EDA (gene distribution, class distribution, chromosome distribution)

Documentation: Full system documentation


🔄 In Progress

Pipeline Integration: End‑to‑end agentic pipeline integration

RAG Optimization: Retrieval and generation tuning

Verification Module: Hallucination detection fine‑tuning

Benchmarking: Comprehensive evaluation on ClinVar test set

Manuscript: Paper preparation



---

🚀 Installation

git clone https://github.com/yourusername/PathogenAgent.git    
cd PathogenAgent    
pip install -r requirements.txt  
  
Requirements  
  
torch>=2.0.0    
transformers>=4.30.0    
sentence-transformers>=2.2.0    
faiss-cpu>=1.7.4    
numpy>=1.24.0    
pandas>=2.0.0    
scikit-learn>=1.3.0    
scipy>=1.10.0    
matplotlib>=3.7.0    
seaborn>=0.12.0    
tqdm>=4.65.0    
requests>=2.31.0    
biopython>=1.81    
gradio>=4.0.0    
reportlab>=4.0.0    
statsmodels>=0.14.0  
  
  
---  
  
📄 License  
  
MIT License  
  
  
---  
  
👤 Author  
  
Vania Karimi  
  
  
---  
  
📎 Related Work  
  
· Fine‑tuned BioGPT: Sepideh2027/biogpt-clinvar-finetuned  
· ClinVar Dataset: Sepideh2027/clinvar-project-backup  
  
  
---  
  
📧 Contact  
  
For questions or collaborations, please open an issue.  
  
  
---  
  
🙏 Acknowledgments  
  
· NCBI for open access to ClinVar, PubMed, and GenBank  
· Hugging Face for model hosting and infrastructure  
· BioGPT team for the base architecture  
  
  
---  
  
---    
    
.** 🚀
