# Mpox Therapeutic Target Discovery Using Bioinformatics and Computer-Aided Drug Design (CADD)

## Overview

This project presents an integrated Bioinformatics and Computer-Aided Drug Design (CADD) workflow for the identification of conserved therapeutic targets and potential inhibitory compounds against the Mpox virus (MPXV).

The study combines comparative genomics, orthogroup analysis, subtractive proteomics, structural bioinformatics, molecular docking, ADMET profiling, and Density Functional Theory (DFT)-based Frontier Molecular Orbital (FMO) analysis to identify druggable viral proteins and prioritize potential antiviral compounds.

A total of 28 Mpox virus genomes representing multiple viral clades were analyzed to identify conserved proteins suitable for broad-spectrum antiviral development.

---

## Objectives

- Identify conserved proteins across diverse Mpox virus lineages.
- Prioritize essential viral proteins lacking homology to human proteins.
- Evaluate structural druggability of shortlisted targets.
- Screen potential inhibitory compounds through molecular docking.
- Assess pharmacokinetic and toxicity profiles using ADMET analysis.
- Evaluate electronic properties of lead compounds through DFT-based FMO analysis.

---

## Workflow

```text
Genome Collection (NCBI)
          │
          ▼
Comparative Genomics
          │
          ▼
Orthogroup Analysis (OrthoFinder)
          │
          ▼
Functional Annotation
(InterProScan + UniProt)
          │
          ▼
Essential Protein Identification
          │
          ▼
Subtractive Proteomics
(BLASTp against Human Proteome)
          │
          ▼
Structural Modelling
(PDB / SWISS-MODEL)
          │
          ▼
Structure Validation
(PROCHECK, VERIFY3D, ERRAT)
          │
          ▼
Binding Pocket Identification
(ProteinPlus)
          │
          ▼
Pocket-Domain Association Analysis
          │
          ▼
Molecular Docking
(AutoDock Vina)
          │
          ▼
ADMET Screening
(SwissADME + pkCSM)
          │
          ▼
DFT-Based FMO Analysis
          │
          ▼
Lead Compound Prioritization
```

---

## Methodology

### Comparative Genomics and Orthogroup Analysis

Twenty-eight complete Mpox virus genomes representing Clades Ia, Ib, IIa, and IIb were retrieved from NCBI GenBank and analyzed using OrthoFinder to identify conserved orthologous proteins across diverse viral strains.

### Functional Annotation and Target Prioritization

Conserved proteins were functionally characterized using InterProScan and UniProt. Essential proteins involved in viral replication, transcription, virion assembly, and host-virus interactions were prioritized.

### Subtractive Proteomics

BLASTp analysis against the human proteome was performed to eliminate proteins with significant similarity to host proteins, reducing potential off-target effects.

### Structural Bioinformatics

Experimentally resolved structures were obtained from the Protein Data Bank (PDB), while unresolved proteins were modeled using SWISS-MODEL and validated using PROCHECK, VERIFY3D, and ERRAT. 

### Structure-Based Drug Discovery

Druggable binding pockets were identified using ProteinPlus. Molecular docking was performed using AutoDock Vina, followed by ADMET evaluation using SwissADME and pkCSM. 

### Quantum Chemical Analysis

Lead compounds were further analyzed using Density Functional Theory (DFT)-based Frontier Molecular Orbital (FMO) analysis to evaluate molecular reactivity, stability, and electronic properties.

---

## Key Findings

- 28 Mpox virus genomes analyzed.
- 198 orthogroups identified.
- 129 conserved single-copy orthogroups detected across all genomes.
- Progressive filtering reduced the dataset to 13 high-confidence therapeutic targets containing 35 biologically relevant binding pockets. 
- Five lead compounds were prioritized through docking, ADMET, redocking validation, and DFT analysis:
  - PubChem CID 3131912
  - PubChem CID 2368032
  - PubChem CID 46360552
  - PubChem CID 3410901
  - PubChem CID 21005142 

---

## Repository Structure

```text
.
├── README.md
├── LICENSE
│
├── docs/
│   └── project_report.pdf
│
├── data/
│   ├── 21005142.sdf
│   ├── 2368032.sdf
│   ├── 3131912.sdf
│   ├── 3410901.sdf
│   ├── 46360552.sdf
│   │
│   ├── AAL40508.1.fasta
│   ├── AAL40508.1_structure.pdb
│   │
│   ├── AAL40517.1.fasta
│   ├── AAL40517.1_structure.pdb
│   │
│   ├── AAL40575.1.fasta
│   ├── AAL40575.1_structure.pdb
│   │
│   ├── AAL40576.1.fasta
│   └── AAL40576.1_structure.pdb
│
├── figures/
│   ├── Orthofinder_Statistics.png
│   ├── Phylogenetic_Tree.png
│   ├── SWISSMODEL_Output.png
│   ├── Binding_Pocket_and_Active_Site.png
│   ├── Docked_Complex.png
│   ├── 2D_Interaction_Map.png
│   └── HOMO_LUMO.png
│
├── supplementary/
│   └── Supplementary Tables.xlsx
│
└── docs/
    └── project_report.pdf
```
│
├── figures/
│   ├── Orthofinder_Statistics.png
│   ├── Phylogenetic_Tree.png
│   ├── SWISSMODEL_Output.png
│   ├── Binding_Pocket_and_Active_Site.png
│   ├── Docked_Complex.png
│   ├── 2D_Interaction_Map.png
│   └── HOMO_LUMO.png
│
└── supplementary/
    └── Supplementary Tables.xlsx
```

---

## Tools and Databases

- NCBI GenBank
- Nextclade
- OrthoFinder
- MAFFT
- Galaxy Europe
- InterProScan
- UniProt
- BLASTp
- Protein Data Bank (PDB)
- SWISS-MODEL
- SAVES Server
- ProteinPlus
- PyMOL
- Open Babel
- AutoDock Vina
- SwissADME
- pkCSM
- Python

---

## Figures

The `figures/` directory contains representative outputs from major stages of the workflow, including:

- Orthogroup analysis
- Phylogenetic analysis
- Structural modelling
- Binding pocket identification
- Molecular docking
- Protein–ligand interaction analysis
- HOMO–LUMO visualization

---

## Supplementary Material

Detailed datasets, filtering results, docking outputs, ADMET evaluations, quantum chemical descriptors, and supporting tables are provided in the `supplementary/` directory.

---

## Disclaimer

This repository is intended for academic, educational, and research purposes. All computational findings require experimental validation before biological or therapeutic application.

---

## Author

**B. Sachithananda Reddy**
