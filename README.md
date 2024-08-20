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
The issue of food security remains a major global challenge (Berry, 2020). Rice is one of the most universally cultivated and crucial staple crops globally. Rice is the main food staple for over half of the global population, especially in Asia (Bandumula, 2018). The importance of rice genomics in advancing breeding efforts is growing significantly. Genetic diversity and gene editing techniques like mutagenesis and genetic transformation are also crucial in rice breeding (Ram et al., 2019). Oryza species are attacked by numerous pathogens, with the most virulent being Xanthomonas oryzae pv. oryzae (Xoo). Xanthomonas oryzae, a major plant pathogen, significantly threatens rice cultivation, resulting in considerable agricultural losses worldwide (Niño-Liu et al., 2006). The interaction between X. oryzae and its rice host is complex, involving detailed molecular and biochemical processes that facilitate infection and spread (Deb et al., 2021). Understanding these plant-pathogen interactions is vital for developing effective strategies to combat the disease and reduce its impact on global food security (Yang et al., 2024). Despite advancements in research, significant gaps remain in the knowledge of infection mechanisms, host resistance, and pathogen adaptation. A detailed understanding of these interactions is essential for creating effective strategies to combat these diseases, ensuring food security and sustainable rice production on a global scale (Ahmad Rizal et al., 2024). Closing these gaps is essential for developing sustainable solutions to safeguard rice crops from X. oryzae and maintain stable rice production for the expanding global population.

The significance of this research includes grasping the interactions between X. oryzae and its rice host is crucial for improving rice production, securing food supplies, encouraging sustainable agricultural practices, promoting a healthier environment and biodiversity and advancing scientific research.

## Aim of the study
This study aims to identify a core set of genes and miRNAs involved in rice's defense response to Xoo and to elucidate the regulatory networks governing these responses through analysis of the publicly available rice RNA-seq data sets associated with the infections of Xoo. Specifically, we:
- Systematically identify previously reported genes and miRNAs associated with rice response to Xoo infection.
- Computationally infer the regulatory relationships between these genes using time-series expression data.
- Analyze the networks to identify key regulatory elements and pathways crucial for Xoo defense.

## Dataset
Time-series RNAseq data used for the project is available [here](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE95668),  [here](https://www.ncbi.nlm.nih.gov/sra/SRX7203160[accn])
miRNA expression data used for the project is available [here]

## Methodology
Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.

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
