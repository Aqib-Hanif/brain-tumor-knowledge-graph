# 🧠 Explainable Brain Tumor Knowledge Graph (X-BrainKG)

## Overview

This repository presents an explainable, domain-specific knowledge graph for brain tumors. The system integrates genes, diseases, and drugs into a structured graph representation, with a focus on interpretability and biomedical relevance.

The objective is to move beyond simple data integration and enable meaningful reasoning over biological relationships, particularly in the context of precision medicine. The graph is designed to capture subtype-level disease information and incorporate evidence-aware relationships to support reliable interpretation.

---

## Motivation

Biomedical knowledge is often fragmented across genomic studies, clinical reports, and pharmacological data sources. Traditional approaches face several challenges:

- Lack of unified representation across heterogeneous data  
- Limited support for molecular subtypes (e.g., IDH mutation status)  
- Absence of interpretability in relationship modeling  
- No explicit representation of evidence or confidence  

This project addresses these issues by constructing a focused knowledge graph that emphasizes structure, evidence, and explainability.

---

## Key Contributions

- Subtype-aware disease modeling using molecular characteristics (e.g., IDH mutation status)  
- Evidence-aware relationships including source, confidence score, and evidence type  
- Explainable reasoning mechanism based on graph traversal  
- Graph-based evaluation including structural validation, query testing, and ablation study  

---

## Knowledge Graph Design

### Node Types
- Disease (brain tumor subtypes)  
- Gene (molecular biomarkers)  
- Drug (therapeutic agents)  

### Relationship Types
- MUTATED_IN (Gene → Disease)  
- TREATS (Drug → Disease)  
- TARGETS (Drug → Gene)  
- ASSOCIATED_WITH (Gene → Disease)  

---

## Explainable Reasoning

A central feature of this system is its ability to generate interpretable reasoning paths.

Example:

Temozolomide → MGMT → Glioblastoma

Interpretation:
- Temozolomide interacts with MGMT (a DNA repair gene)  
- MGMT is associated with Glioblastoma  
- This provides a biological explanation for treatment effectiveness  

---

## Project Structure

BrainTumor-KG/
│
├── data/
│   └── brain_tumor_edges.csv
│
├── figures/
│   ├── graph_visualization.png
│   ├── degree_distribution.png
│   └── relationship_distribution.png
│
├── notebooks/
│   └── brain_tumor_kg.ipynb
│
├── results/
│   ├── brain_tumor_kg.gexf
│   └── summary.json
│
├── requirements.txt
├── README.md
└── .gitignore

---

## Installation

Clone the repository:

git clone https://github.com/Aqib-Hanif/brain-tumor-knowledge-graph.git  
cd brain-tumor-knowledge-graph  

Install dependencies:

pip install -r requirements.txt  

---

## Usage

Run the Jupyter Notebook:

notebooks/brain_tumor_kg.ipynb  

The notebook includes:
- Graph construction  
- Attribute enrichment  
- Evidence modeling  
- Explainable reasoning  
- Visualization  
- Evaluation and ablation study  

---

## Results

The system demonstrates:
- Integration of biomedical entities into a structured graph  
- Query-based retrieval of clinically relevant relationships  
- Generation of interpretable reasoning paths  
- Evidence-aware relationship modeling  

Graph Statistics:
- Nodes: 7  
- Edges: 6  
- Density: 0.1429  

---

## Experimental Design

Baseline Graph:
- No attributes  
- No evidence modeling  
- No reasoning  

Proposed Graph (X-BrainKG):
- Attribute-enriched nodes  
- Evidence-aware edges  
- Explainable reasoning  

Ablation Study:
- Removal of node attributes  
- Removal of evidence metadata  
- Removal of reasoning module  

Each component contributes to improved interpretability and usability.

---

## Limitations

- Small, manually curated dataset  
- Limited number of entities and relationships  
- Rule-based reasoning  

---

## Future Work

- Integration with large-scale datasets (TCGA, DrugBank)  
- Inclusion of pathways and phenotypes  
- Graph Neural Networks (GNNs)  
- Automated extraction from biomedical literature  

---

## License

This project is intended for academic and research purposes.

---

## Author

Aqib Hanif  
GitHub: https://github.com/Aqib-Hanif