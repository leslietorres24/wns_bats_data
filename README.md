# White-Nose Syndrome Multi-Omics Project  
**Leslie Torres | BIOL F493 – Microbial Metagenomics | University of Alaska Fairbanks**

---

### 🦇 Overview  
This repository contains reproducible workflows and scripts used to investigate *Pseudogymnoascus destructans* (Pd) infection mechanisms, host immune responses in North American bats, and potential probiotic antifungal interactions using *Streptomyces albidoflavus*.  

All analyses are conducted **in silico** using publicly available data and open-source computational tools.  
This project combines **Galaxy**, **Anvi’o**, and **R/Bioconductor** workflows to demonstrate cross-platform bioinformatics proficiency.  

---

### 🎯 Research Aims  
1. **Fungal Gene Expression & Pathogenicity**  
   - Analyze *P. destructans* transcriptomes (infection vs culture).  
   - Identify genes involved in virulence, cold adaptation, and stress response.  

2. **Probiotic Antifungal Genomics** *(Predictive / Exploratory)*  
   - Annotate *Streptomyces albidoflavus SM254* genome.  
   - Identify biosynthetic gene clusters (BGCs) with antifungal potential.  

3. **Bat Host Transcriptomics**  
   - Characterize immune and metabolic pathways in *Myotis lucifugus* during Pd infection.  
   - Explore cross-species differences in *Myotis myotis* and *M. septentrionalis*.  

---

### 🧫 Datasets  

| Organism | Source / Study | BioProject ID | Data Type | Use |
|-----------|----------------|----------------|-------------|------|
| *Pseudogymnoascus destructans* | Palmer et al., 2018 | PRJNA400424 | RNA-seq | Infection vs culture (fungal DE) |
| *Pseudogymnoascus destructans* | Minnis & Lindner, 2018 | PRJNA262909 | Genome assembly | Reference for mapping |
| *Myotis lucifugus* | Field et al., 2015 | PRJNA274372 | RNA-seq | Bat immune response |
| *Streptomyces albidoflavus* SM254 | Popov et al., 2025 | PRJNA983047 | Genome | BGC prediction |
| *Streptomyces albidoflavus* | Jönsson et al., 2025 | PRJNA915879 | RNA-seq compendium | BGC co-expression |
| *Myotis myotis* | Riquier et al., 2025 | PRJNA1017783 | RNA-seq | Comparative host response |

---

### ⚙️ Workflow Summary  

**Primary Analysis in Galaxy**
1. Quality Control: FastQC → Trimmomatic  
2. Mapping: HISAT2 → BAM alignments  
3. Read Quantification: FeatureCounts  
4. Differential Expression: DESeq2  
5. GO/KEGG Enrichment: clusterProfiler  

**Secondary Analysis in Anvi’o**
- Genome annotation and visualization (Pd, SM254)  
- Pangenome analysis for *Pseudogymnoascus* spp.  
- Integration of antiSMASH BGC predictions  

**Integration**
- Combine DESeq2 results (Galaxy/R) with genomic annotation (Anvi’o).  
- Visualize high-expression or virulence-associated regions.

---

### 🧠 Tools & Versions
| Tool | Version | Purpose |
|------|----------|----------|
| Galaxy | v24+ | Workflow execution (RNA-seq) |
| FastQC | v0.12.1 | Read quality assessment |
| Trimmomatic | v0.39 | Read trimming |
| HISAT2 | v2.2.1 | Alignment |
| featureCounts | v2.0.3 | Quantification |
| DESeq2 | v1.42.0 | Differential expression |
| clusterProfiler | v4.10 | Functional enrichment |
| Anvi’o | v7+ | Genome visualization / pangenomics |
| antiSMASH | v7+ | Secondary metabolite cluster prediction |

---

### 🧩 Repository Structure

