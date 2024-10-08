![DenD](https://img.shields.io/badge/Project-xanthomonasppi-lightblue)
[![Open In Collab](https://colab.research.google.com/assets/colab-badge.svg)](xxxxxx)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Python](https://img.shields.io/badge/python-3.12-blue.svg)
[![GitHub contributors](https://img.shields.io/github/contributors/omicscodeathon/denguedrug.svg)](https://GitHub.com/omicscodeathon/xanthomonasppi/graphs/contributors/)


# Plant-pathogen interactions between _Xanthomonas oryzae_ and its host
## Table of contents
1. [Background](#background)
2. [Study aim](#aim-of-the-study)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Credits](#credits)

![image](https://github.com/omicscodeathon/xanthomonasppi/blob/main/images/Interaction-model-between-pathogen-and-rice.png)

Source: [Yang et. al, 2022](https://www.researchgate.net/figure/Interaction-model-between-pathogen-and-rice_fig2_359419059)

## Background
The issue of food security remains a major global challenge (Berry, 2020). Rice is one of the most universally cultivated and crucial staple crops globally. Rice is the main food staple for over half of the global population, especially in Asia (Bandumula, 2018). Rice is not just a vital food source but also a cultural staple in many societies, symbolizing prosperity and life in various traditions around the world(Krisnawati et al., 2024). The importance of rice genomics in advancing breeding efforts is growing significantly. Genetic diversity and gene editing techniques like mutagenesis and genetic transformation are also crucial in rice breeding (Ram et al., 2019). Oryza species are attacked by numerous pathogens, with the most virulent being Xanthomonas oryzae pv. oryzae (Xoo). Xanthomonas oryzae is a gram-negative bacterium that causes two significant rice diseases: bacterial leaf blight (BLB) and bacterial leaf streak (BLS). These diseases are among the most destructive to rice crops globally, leading to substantial reductions in both yield and quality (Niño-Liu et al., 2006, Jiang et al., 2020). Xanthomonas oryzae pv. oryzae (Xoo), is the pathogen behind bacterial leaf blight, while Xanthomonas oryzae pv. oryzicola (Xoc), causes bacterial leaf streak(Jiang et al., 2020).
The interaction between X. oryzae and its rice host is complex, involving detailed molecular and biochemical processes that facilitate infection and spread (Deb et al., 2021). Xanthomonas oryzae infects rice plants through natural openings, such as stomata or wounds, and can also penetrate through damaged areas(Kumar et al., 2020). Once inside, it releases effector proteins that interfere with the host's cellular functions, promoting bacterial survival and replication(Jamaloddin et al., 2021). Rice plants recognize these pathogens through immune receptors and trigger defensive responses, including the production of reactive oxygen species and antimicrobial peptides. Despite this, some of X. oryzae's effectors can overcome these defenses, leading to greater susceptibility and resulting in symptoms like leaf blight or streaks. The bacteria can spread within the plant and to nearby plants, causing substantial crop damage. The impact of the disease is also influenced by host factors, such as the rice variety's resistance or susceptibility(Jamaloddin et al., 2021). Grasping the intricate molecular mechanisms of this interaction is essential for creating effective disease management strategies. This includes breeding rice varieties that are resistant to the pathogen, using specific chemical treatments, and devising comprehensive pest management approaches(Yang et al., 2024).
Despite advancements in research, significant gaps remain in the knowledge of infection mechanisms, host resistance, and pathogen adaptation. A detailed understanding of these interactions is essential for creating effective strategies to combat these diseases, ensuring food security and sustainable rice production on a global scale (Ahmad Rizal et al., 2024). Closing these gaps is essential for developing sustainable solutions to safeguard rice crops from X. oryzae and maintain stable rice production for the expanding global population.

The significance of this research includes grasping the interactions between X. oryzae and its rice host is crucial for improving rice production, securing food supplies, encouraging sustainable agricultural practices, promoting a healthier environment and biodiversity and advancing scientific research.

## Aim of the study
This study aims to identify a core set of genes and miRNAs involved in rice's defense response to Xoo and to elucidate the regulatory networks governing these responses through analysis of the publicly available rice RNA-seq data sets associated with the infections of Xoo. Specifically, we:
- Systematically identify previously reported genes and miRNAs associated with rice response to Xoo infection.
- Computationally infer the regulatory relationships between these genes using time-series expression data.
- Analyze the networks to identify key regulatory elements and pathways crucial for Xoo defense.

## Dataset
Time-series RNAseq data used for the project is available [here](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE95668),  [here](https://www.ncbi.nlm.nih.gov/sra/SRX7203160[accn]) and [here](https://www.ncbi.nlm.nih.gov/sra/?term=SRP232925). While miRNA expression data used for the project is available [here](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE141996) and [here](https://www.ncbi.nlm.nih.gov/sra/SRX6406229[accn]).

## Methodology
**1. Data Preprocessing:**

The raw sequencing data was initially subjected to quality control using the FastQC tool, followed by a comprehensive multi-sample quality report generated with MultiQC. To ensure high-quality reads, trimming was performed using Fastp, removing low-quality bases and adapter sequences. Normalization of the read counts was carried out using the Trimmed Mean of M-values (TMM) method to account for compositional differences between samples.

**- Read Alignment and Gene Expression Quantification:**

Post-trimming, the clean reads were aligned to the rice reference genome (GCF_034140825.1) using the HISAT2 aligner, which provides a high level of accuracy and efficiency for spliced alignments. The aligned reads were then used to quantify gene expression levels with HTSeq, generating count data for downstream differential expression analysis.

**2. Differential Expression Analysis**

**- miRNA Data Analysis:**

Differentially expressed genes (DEGs) were identified using the limma statistical package, which is well-suited for the analysis of miRNA data due to its robustness in handling small datasets.

**- RNA-Seq Analysis:**

For RNA-seq data, the STAR aligner was employed to perform high-throughput read alignment, ensuring accurate mapping to the reference genome. Quantification of gene expression was then conducted, followed by the identification of DEGs using the DESeq2 package, which offers precise normalization and statistical testing for differential expression.

**- miRNA Differential Expression:**

To identify differentially expressed miRNAs (DEMs), the miRDeep2 suite was utilized. This tool is specifically designed for miRNA analysis, providing sensitive detection and quantification of miRNAs across samples.

**3. Inference of Regulatory Relationships**

**- Time-Series Analysis:**

To capture dynamic expression patterns of genes and miRNAs over time, a comprehensive time-series analysis was performed using a combination of DESeq2, edgeR, maSigPro, and ImpulseDE2. These tools collectively provide robust statistical methods for identifying temporal changes in expression and detecting differentially expressed genes and miRNAs across time points.

**- Gene Regulatory Network Construction:**

Gene regulatory networks (GRNs) were constructed using GRNBoost2, a tool that leverages machine learning algorithms to infer regulatory interactions from expression data. This approach enabled the identification of key regulatory relationships among genes.

**- miRNA-Target Interaction Prediction:**

miRNA-target interactions were predicted using the miRanda algorithm, which is specifically designed to identify potential miRNA binding sites on target mRNAs. This tool facilitates the discovery of regulatory roles of miRNAs by predicting their target genes within the inferred GRNs.

**4. Network Analysis and Key Element Identification**

**- Network Visualization and Analysis:**

The inferred gene regulatory networks were visualized and analyzed using Cytoscape, an advanced tool for the graphical representation and exploration of complex biological networks. This facilitated the interpretation of network topology and interactions.

**- Functional Enrichment Analysis:**

To elucidate the biological significance of differentially expressed genes (DEGs) and their predicted target genes, functional enrichment analysis was conducted using DAVID. This involved Gene Ontology (GO) and KEGG pathway analyses to identify enriched biological processes, molecular functions, and pathways, offering insights into the potential roles of these genes in the studied biological context.

**- Identification of Key Regulatory Elements:**

Key regulatory elements within the network, including hub genes and miRNAs, were identified by calculating centrality measures such as degree, betweenness, and closeness. These metrics helped to pinpoint the most influential nodes within the network, providing a deeper understanding of the regulatory architecture.

**5. Validation and Functional Annotation**

**- Computational Validation:**

The computational predictions were validated using miRanda, a specialized tool for miRNA-target interaction analysis. This validation step ensured the accuracy and reliability of the identified miRNA-target pairs.

**- Functional Annotation and Visualization:**

To further explore the biological relevance of the validated findings, functional annotation was performed using DAVID. The tool’s visualization capabilities were employed to generate informative plots, such as GO term enrichment and KEGG pathway maps, facilitating a clearer understanding of the functional roles of the identified genes and miRNAs.


## Workflow
![workflow](https://github.com/omicscodeathon/xanthomonasppi/blob/main/images/xooppi_workflow.png)

## Requirements for using this pipeline
Programming platforms
```{r}
R
Python 3.12

```
Packages to install
````````
FastQc
Fastp
MultiQC

```{r}
#Grenadine
#Dummy text
```
Bash script
```{r}
#This is a dummy text
```

## Pipeline Summary
Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.

## Credits
1. [Samuel K.T. Owusu-Ansah](https://github.com/sktowusuansah), Department of Soil and Crop Sciences, Colorado State University, Fort Collins, USA | Project/Tech Lead
2. [Akachukwu Onwuka](https://github.com/Akachukwuebuka), Department of Pharmacology and Toxicology, Faculty of Pharmaceutical Science, University of Nigeria, Nsukka | Writing Lead
3. [Khadija Elamin](https://github.com/Khadijaelamin93), Department of Botany, Faculty of Science, University of Khartoum, Sudan | Pipeline Development & Implementation
4. [Jessica Arthur](https://github.com/Geska7), Genomics and Bioinformatics Laboratory, West African Center for Cell Biology of Infectious Pathogens, University of Ghana, Ghana | Implementation, Analysis & Writing
5. [Paul Ajwang](https://github.com/Ojwang-Biot), MSc. Bioinformatics, Pwani University, Kenya | Analysis, Writing
6. [Reginald Isaya Odongo](https://github.com/OdongoIsaya), MSc. Bioinformatics, Pwani University, Kenya | Analysis, Writing
7. [Olaitan I. Awe](https://github.com/laitanawe), African Society for Bioinformatics and Computational Biology, South Africa | Conceptualisation | Editing
