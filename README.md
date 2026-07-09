# 🧬 PathogenAgentAI

<hr>
<p align="center">
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.11"></a>
  <a href="https://pytorch.org/"><img src="https://img.shields.io/badge/PyTorch-2.x-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch 2.x"></a>
  <a href="https://huggingface.co/docs/transformers/index"><img src="https://img.shields.io/badge/🤗%20Transformers-Latest-F9A8D4?style=for-the-badge" alt="Hugging Face Transformers"></a>
  <a href="https://huggingface.co/Sepideh2027/biogpt-clinvar-finetuned"><img src="https://img.shields.io/badge/🧬%20BioGPT--ClinVar-Fine--tuned-22A699?style=for-the-badge" alt="Fine-tuned BioGPT-ClinVar"></a>
  <a href="https://huggingface.co/docs/peft/en/developer_guides/lora"><img src="https://img.shields.io/badge/PEFT-LoRA-40A578?style=for-the-badge" alt="PEFT LoRA"></a>
  <a href="https://www.ncbi.nlm.nih.gov/clinvar/"><img src="https://img.shields.io/badge/Data-ClinVar-8B0000?style=for-the-badge" alt="ClinVar Data"></a>
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/Status-Active%20Development-FFA500?style=for-the-badge" alt="Status: Active Development"></a>
  <a href="#"><img src="https://img.shields.io/badge/Research-AI%20for%20Science-6A0DAD?style=for-the-badge" alt="Research: AI for Science"></a>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-3D9970?style=for-the-badge" alt="License: MIT"></a>
</p>

<p align="center">
  <strong>A Modular Platform for Biomedical Data Engineering and Foundation Model Integration</strong>
</p>

---

> **Current Status**
>
> PathogenAgentAI is an actively developed research platform.
>
> The biomedical data engineering pipeline, dataset construction workflow, BioGPT integration, and an interactive biomedical inference and UniProt evidence retrieval prototype have been implemented.
>
> Retrieval-Augmented Generation (RAG), evidence integration, and agentic reasoning modules are currently under development.

---

## Overview

PathogenAgentAI is a modular scientific software platform designed for large-scale biomedical language model applications.

Unlike conventional machine learning repositories that focus exclusively on model training, this project emphasizes the complete computational workflow required to build reproducible biomedical AI systems—from raw genomic data processing to deployable inference pipelines.

The current implementation integrates large-scale ClinVar data engineering with a previously fine-tuned BioGPT language model while establishing the software architecture required for future evidence-aware genomic reasoning.

Although the present version is developed using human genomic variant data, the underlying software architecture is intentionally organism-agnostic and designed to support future extensions toward pathogen genomics, genomic surveillance, and computational epidemiology.

---

## Motivation

Modern biomedical AI systems increasingly require more than accurate predictive models.

They require:

- scalable biomedical data engineering
- reproducible computational pipelines
- reusable scientific software
- transparent experimentation
- modular architectures that can evolve with future research

PathogenAgentAI was developed to address these engineering challenges by separating biomedical data processing, language model integration, software infrastructure, and future reasoning components into independent, reusable modules.

This philosophy enables the platform to serve as a foundation for future AI systems in genomics, computational biology, and AI for Science.

---

## Key Features

- Large-scale biomedical data engineering pipeline
- Processing of **8.99 million** structured ClinVar records
- Automated quality control and biological filtering
- Curated dataset containing **4.21 million** machine-learning-ready genomic variants
- Gene-aware dataset partitioning to reduce biological information leakage
- BioGPT integration using a companion fine-tuned biomedical language model
- Parameter-efficient model adaptation through LoRA
- Modular software architecture
- Interactive inference demonstration
- Fully reproducible research workflow

---

## Companion Project

The BioGPT model used by PathogenAgentAI originates from the companion research project:

> **BioGPT-ClinVar: Parameter-Efficient Fine-Tuning of a Biomedical Language Model for Genomic Variant Interpretation**

The two repositories have distinct objectives.

| BioGPT-ClinVar | PathogenAgentAI |
|----------------|-----------------|
| Language model adaptation | Scientific AI software platform |
| BioGPT fine-tuning | Biomedical data engineering |
| LoRA training | Modular infrastructure |
| Model publication | End-to-end research workflow |
| Hugging Face model | Future AI reasoning architecture |

PathogenAgentAI reuses the fine-tuned BioGPT model as its language model backbone while extending it into a broader scientific software ecosystem.

---

## Research Scope

**Current implementation:**

- Biomedical data engineering
- ClinVar preprocessing
- Instruction dataset generation
- BioGPT integration
- Interactive inference
- UniProt evidence retrieval prototype

**Planned extensions:**

- Retrieval-Augmented Generation (RAG)
- Biomedical evidence retrieval
- Multi-source knowledge integration
- Reflection and verification modules
- Agentic scientific reasoning
- Pathogen genomic analysis

---

## High-Level Architecture

```text
                    ┌──────────────────────────────────────────┐
                    │           PathogenAgentAI                │
                    └──────────────────────────────────────────┘

         Biomedical Data Layer                Scientific AI Layer

 ┌──────────────────────────────┐     ┌──────────────────────────────┐
 │                              │     │                              │
 │  Data Engineering Pipeline   │ ──► │  BioGPT Inference Platform   │
 │                              │     │                              │
 │  • Data Processing           │     │  • Model Loading             │
 │  • Quality Control           │     │  • Interactive Demo          │
 │  • Feature Engineering       │     │  • Inference Pipeline        │
 │  • Dataset Generation        │     │  • Future RAG Modules        │
 │                              │     │                              │
 └──────────────────────────────┘     └──────────────────────────────┘
```

---

Architectural Design Principles

The software architecture was designed according to five engineering principles.

1. Modularity — Each computational component performs a single well-defined task, enabling independent testing, maintenance, and future replacement.

2. Reproducibility — Every preprocessing stage follows deterministic workflows. Dataset construction, quality control, feature engineering, and model preparation can be reproduced from the original ClinVar release.

3. Scalability — The architecture supports biomedical datasets containing millions of genomic variants while remaining extensible to future pathogen genomic resources.

4. Separation of Concerns — Preprocessing, modeling, and deployment are implemented as independent components, simplifying future experimentation and collaborative development.

5. Extensibility — Although the current implementation focuses on ClinVar-derived genomic variants, the software architecture remains organism-agnostic.

---

Current Software Components

Module Status
Biomedical Data Processing ✅ Implemented
Automated Quality Control ✅ Implemented
Feature Engineering ✅ Implemented
Dataset Statistics ✅ Implemented
Gene-aware Dataset Splitting ✅ Implemented
Instruction Dataset Generation ✅ Implemented
BioGPT Integration ✅ Implemented
Interactive Inference Demo ✅ Implemented
UniProt Evidence Retrieval Prototype ✅ Implemented

---

Planned Platform Components

Future Module Status
Retrieval-Augmented Generation (RAG) 🚧 Planned
Biomedical Evidence Retrieval 🚧 Planned
Reflection Module 🚧 Planned
Evidence Verification 🚧 Planned
Confidence Estimation 🚧 Planned
Multi-Agent Scientific Workflow 🚧 Planned

---

Biomedical Data Engineering Pipeline

A major objective of PathogenAgentAI is to establish a fully reproducible biomedical data engineering workflow capable of transforming raw clinical genomic repositories into machine-learning-ready corpora.

Rather than relying on preprocessed benchmark datasets, the entire preprocessing pipeline was designed and implemented from scratch, allowing every transformation step—from raw data ingestion to final model-ready datasets—to remain transparent, reproducible, and biologically consistent.

---

Data Source

The project is built upon ClinVar, one of the largest publicly available repositories of clinically annotated genomic variants maintained by the National Center for Biotechnology Information (NCBI).

---

Dataset Statistics

Processing Stage Records
Structured ClinVar records 8,991,566
After automated quality control 8,500,622
Final curated biological dataset 4,216,934
Training dataset 2,690,964
Validation dataset 725,719
Test dataset 800,251

---

Pipeline Overview

```text
ClinVar
    │
    ▼
Structured Parsing
    │
    ▼
Quality Control
    │
    ▼
Biological Filtering
    │
    ▼
Feature Engineering
    │
    ▼
Gene-aware Dataset Split
    │
    ▼
Instruction Dataset Generation
    │
    ▼
BioGPT-ready Dataset
```

---

Stage 1 — Structured Parsing

From the original ClinVar release, biologically relevant attributes were extracted, including gene symbol, clinical significance, chromosome, genomic position, and genome assembly.

8,991,566 genomic variant records were processed.

---

Stage 2 — Automated Quality Control

A dedicated quality control pipeline performs missing value removal, malformed record filtering, unsupported annotation removal, and normalization of clinical significance labels.

After quality control: 8,500,622 high-quality genomic variants.

---

Stage 3 — Biological Dataset Curation

Task-specific preprocessing and biological filtering were applied to retain clinically informative variants suitable for downstream language model adaptation.

Final curated dataset: 4,216,934 biologically curated genomic variants.

---

Stage 4 — Gene-aware Dataset Partitioning

To reduce biological information leakage, a gene-aware partitioning strategy was implemented, ensuring variants from the same gene do not appear across training and evaluation sets.

Split Records
Training 2,690,964
Validation 725,719
Test 800,251

---

Stage 5 — Instruction Dataset Generation

Curated genomic records were transformed into instruction-style supervision suitable for biomedical language model adaptation, following an instruction–response paradigm.

---

Tokenization Pipeline

The complete dataset was tokenized using the BioGPT tokenizer with parallel tokenization via Hugging Face Datasets, producing tokenized inputs, attention masks, and target labels.

---

Engineering Principles

The biomedical preprocessing workflow follows four design principles: biological consistency, reproducibility, scalability, and modularity.

---

BioGPT Integration

PathogenAgentAI does not train a biomedical language model from scratch. Instead, it integrates a previously developed domain-adapted BioGPT model into a larger scientific software ecosystem.

Companion Model

The fine-tuned language model is publicly available on Hugging Face:

https://img.shields.io/badge/🤗%20Hugging%20Face-Model-ffd21e

biogpt-clinvar-finetuned
A parameter-efficient adaptation of BioGPT for clinical genomic variant interpretation using Low-Rank Adaptation (LoRA).

BioGPT-ClinVar (Companion) PathogenAgentAI
Biomedical language model adaptation Scientific AI software platform
LoRA fine-tuning Biomedical data engineering
Model optimization Modular computational infrastructure
Hugging Face model release Interactive research platform
Training pipeline End-to-end biomedical workflow

---

Model Backbone

Property Value
Base Model BioGPT (microsoft/biogpt)
Adaptation Method Low-Rank Adaptation (LoRA)
Domain Biomedical NLP
Task Clinical Genomic Variant Interpretation
Availability Public on Hugging Face

---

Why BioGPT?

BioGPT was selected for its biomedical pretraining, domain-specific contextual representations, compatibility with clinical terminology, and efficient adaptation through parameter-efficient fine-tuning.

---

Parameter-Efficient Adaptation

The underlying language model was adapted using Low-Rank Adaptation (LoRA), which introduces trainable low-rank matrices while keeping the pretrained backbone frozen. This approach provides lower GPU memory requirements, faster experimentation, reduced training cost, improved reproducibility, and easier adaptation to future tasks.

---

Usage

You can load and use the fine-tuned model directly from Hugging Face:

```python
from peft import PeftModel
from transformers import AutoModelForCausalLM, AutoTokenizer

# Load base model and tokenizer
base_model = AutoModelForCausalLM.from_pretrained("microsoft/biogpt")
tokenizer = AutoTokenizer.from_pretrained("microsoft/biogpt")

# Load LoRA adapter
model = PeftModel.from_pretrained(base_model, "Sepideh2027/biogpt-clinvar-finetuned")

# Generate prediction
inputs = tokenizer("Your biomedical input text here", return_tensors="pt")
outputs = model.generate(**inputs, max_length=128)
print(tokenizer.decode(outputs[0]))
```

Alternative inference options:

Method Command / Usage
Transformers Pipeline pipe = pipeline("text-generation", model="Sepideh2027/biogpt-clinvar-finetuned")
vLLM Server vllm serve "Sepideh2027/biogpt-clinvar-finetuned"
SGLang Server python3 -m sglang.launch_server --model-path "Sepideh2027/biogpt-clinvar-finetuned"
Docker docker model run hf.co/Sepideh2027/biogpt-clinvar-finetuned

---

Current Inference Workflow

```text
Biomedical Input
        │
        ▼
Input Validation
        │
        ▼
BioGPT Tokenizer
        │
        ▼
Fine-tuned BioGPT Model (LoRA)
        │
        ▼
Generated Biomedical Interpretation
        │
        ▼
Structured Output
```

---

Planned Extensions

· Retrieval-Augmented Generation (RAG)
· Biomedical evidence retrieval
· Evidence ranking
· Confidence estimation
· Hallucination verification
· Multi-agent scientific reasoning

---
Interactive Demonstration

PathogenAgentAI includes an interactive research prototype that demonstrates the current biomedical inference and evidence retrieval workflow.

The prototype accepts natural-language biomedical questions through a Gradio interface, retrieves functionally relevant protein annotations from UniProt using dense vector retrieval (Sentence Transformers + FAISS), ranks the retrieved evidence, constructs an evidence-aware context, generates a biomedical response using a language model, and performs a lightweight evidence verification step.

The current implementation serves as a proof-of-concept for the retrieval and inference pipeline that will later be extended into the complete agentic architecture.

Current Prototype Capabilities

· Interactive biomedical question answering
· UniProt knowledge retrieval
· Sentence Transformer embeddings
· FAISS vector similarity search
· Intent routing
· Evidence ranking
· Context construction
· Biomedical response generation
· Basic evidence verification
· Gradio-based web interface

<p align="center">
  <img src="figures/demo.gif" width="850" alt="PathogenAgentAI Demo">
</p>

Current Workflow

```text
Biomedical Question
        │
        ▼
Intent Routing
        │
        ▼
Sentence Embedding
        │
        ▼
FAISS Retrieval
        │
        ▼
Evidence Ranking
        │
        ▼
Context Construction
        │
        ▼
Biomedical Response Generation
        │
        ▼
Evidence Verification
        │
        ▼
Final Response
```

Current Knowledge Source

The current prototype retrieves biomedical evidence exclusively from UniProt protein functional annotations.

Future versions will extend the retrieval layer by integrating additional biomedical resources, including:

· ClinVar
· PubMed
· GenBank

Future Integration

The current prototype represents the first implemented component of the future PathogenAgentAI agentic framework.

Planned extensions include:

· Retrieval-Augmented Generation (RAG)
· Multi-source evidence integration
· Reflection module
· Confidence estimation
· Multi-agent biomedical reasoning

Note: The current demonstration implements the retrieval, evidence ranking, context construction, response generation, and verification pipeline. The complete multi-agent reasoning framework described in the project roadmap is under active development.


---

Repository Structure

```text
PathogenAgentAI/
├── data/
│   ├── preprocessing/
│   ├── statistics/
│   ├── train/
│   ├── validation/
│   └── test/
├── demo/
│   ├── app.py
│   ├── ui/
│   └── assets/
├── models/
│   ├── loader.py
│   ├── inference.py
│   └── tokenizer.py
├── notebooks/
├── docs/
├── figures/
├── README.md
└── LICENSE
```

---

Current Implementation Status

Component Status
ClinVar preprocessing ✅
Biomedical data engineering ✅
Automated quality control ✅
Dataset statistics ✅
Gene-aware dataset partitioning ✅
Instruction dataset generation ✅
BioGPT integration ✅
Interactive inference demo ✅
UniProt evidence retrieval prototype ✅
Modular repository organization ✅

---

Development Roadmap

Phase I — Biomedical Data Engineering (Completed)

· ClinVar processing, quality control, biological filtering, feature engineering, dataset generation, tokenization

Phase II — Foundation Model Integration (Completed)

· BioGPT integration, LoRA-compatible inference, interactive demonstration, modular software architecture

Phase III — Scientific AI Platform (In Progress)

· Retrieval-Augmented Generation, biomedical knowledge retrieval, evidence ranking, reflection workflow, verification pipeline

Phase IV — Future Research (Planned)

· Pathogen genomic databases, knowledge graph integration, agentic biomedical reasoning, public health decision support, computational epidemiology workflows

---

Model Availability

Resource Link
Fine-tuned BioGPT Model (LoRA Adapter) Sepideh2027/biogpt-clinvar-finetuned
ClinVar Dataset Sepideh2027/Agent
BioGPT Instruction Dataset Sepideh2027/Agent

---

Reproducibility

The repository provides documented preprocessing workflows, curated biomedical datasets, reproducible repository organization, and publicly available model and dataset resources, allowing future researchers to reproduce, extend, and reuse the complete computational workflow.

---

Scientific Impact

PathogenAgentAI contributes to biomedical AI research through:

· Large-scale Biomedical Data Engineering — A reproducible pipeline transforming millions of raw ClinVar records into machine-learning-ready datasets
· Gene-aware Dataset Construction — Partitioning by gene identity to reduce biological information leakage
· Scientific Software Architecture — Modular separation of data engineering, model integration, inference, and future reasoning components
· Foundation for Future AI Systems — Organism-agnostic architecture supporting future pathogen genomics, genomic surveillance, and computational epidemiology

---

Citation

If you use this repository in your research, please cite:

```bibtex
@software{Moafi2026_pathogenagentai,
  author       = {Sepideh Moafi},
  title        = {PathogenAgentAI: A Modular Platform for Biomedical Data Engineering and Foundation Model Integration},
  year         = {2026},
  url          = {https://github.com/AIResearcher20/PathogenAgentAI}
}
```

The companion language model is available separately:

biogpt-clinvar-finetuned: https://huggingface.co/Sepideh2027/biogpt-clinvar-finetuned

---

License

This project is released for academic and research purposes. Please see the LICENSE file for additional information.

---

Acknowledgements

This project builds upon publicly available biomedical resources including ClinVar (NCBI), BioGPT, Hugging Face Transformers, PyTorch, PEFT, vLLM, and SGLang. We gratefully acknowledge the open-source community whose tools made this work possible.

---

<p align="center">

PathogenAgentAI

Building trustworthy AI infrastructure for computational biology and AI for Science.

</p>
```

