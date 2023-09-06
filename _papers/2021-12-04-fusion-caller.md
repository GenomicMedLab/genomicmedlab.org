---
layout: paper

title: Discovery of clinically relevant fusions in pediatric cancer
date:  2021-12-04
authors: "Stephanie LaHaye, James R. Fitch, Kyle J. Voytovich, Adam C. Herman, Benjamin J. Kelly, Grant E. Lammi, Jeremy A. Arbesfeld, Saranga Wijeratne, Samuel J. Franklin, Kathleen M. Schieffer, Natalie Bir, Sean D. McGrath, Anthony R. Miller, Amy Wetzel, Katherine E. Miller, Tracy A. Bedrosian, Kristen Leraas, Elizabeth A. Varga, Kristy Lee, Ajay Gupta, Bhuvana Setty, Daniel R. Boué, Jeffrey R. Leonard, Jonathan L. Finlay, Mohamed S. Abdelbaki, Diana S. Osorio, Selene C. Koo, Daniel C. Koboldt, Alex H. Wagner, Ann-Kathrin Eisfeld, Krzysztof Mrózek, Vincent Magrini, Catherine E. Cottrell, Elaine R. Mardis, Richard K. Wilson & Peter White"
journal_cite: " BMC Genomics 22, 872"
doi: https://doi.org/10.1186/s12864-021-08094-z
pmid: 34863095
publisher_url: https://link.springer.com/article/10.1186/s12864-021-08094-z#citeas
github: https://github.com/nch-igm/EnFusion

thumbnail: fusion_caller_paper_preview.png

projects:  # names of lab project(s) to reference
---
### Background

Pediatric cancers typically have a distinct genomic landscape when compared to adult cancers and frequently carry somatic gene fusion events that alter gene expression and drive tumorigenesis. Sensitive and specific detection of gene fusions through the analysis of next-generation-based RNA sequencing (RNA-Seq) data is computationally challenging and may be confounded by low tumor cellularity or underlying genomic complexity. Furthermore, numerous computational tools are available to identify fusions from supporting RNA-Seq reads, yet each algorithm demonstrates unique variability in sensitivity and precision, and no clearly superior approach currently exists. To overcome these challenges, we have developed an ensemble fusion calling approach to increase the accuracy of identifying fusions.

### Results

Our Ensemble Fusion (EnFusion) approach utilizes seven fusion calling algorithms: Arriba, CICERO, FusionMap, FusionCatcher, JAFFA, MapSplice, and STAR-Fusion, which are packaged as a fully automated pipeline using Docker and Amazon Web Services (AWS) serverless technology. This method uses paired end RNA-Seq sequence reads as input, and the output from each algorithm is examined to identify fusions detected by a consensus of at least three algorithms. These consensus fusion results are filtered by comparison to an internal database to remove likely artifactual fusions occurring at high frequencies in our internal cohort, while a “known fusion list” prevents failure to report known pathogenic events. We have employed the EnFusion pipeline on RNA-Seq data from 229 patients with pediatric cancer or blood disorders studied under an IRB-approved protocol. The samples consist of 138 central nervous system tumors, 73 solid tumors, and 18 hematologic malignancies or disorders. The combination of an ensemble fusion-calling pipeline and a knowledge-based filtering strategy identified 67 clinically relevant fusions among our cohort (diagnostic yield of 29.3%), including RBPMS-MET, BCAN-NTRK1, and TRIM22-BRAF fusions. Following clinical confirmation and reporting in the patient’s medical record, both known and novel fusions provided medically meaningful information.

### Conclusions

The EnFusion pipeline offers a streamlined approach to discover fusions in cancer, at higher levels of sensitivity and accuracy than single algorithm methods. Furthermore, this method accurately identifies driver fusions in pediatric cancer, providing clinical impact by contributing evidence to diagnosis and, when appropriate, indicating targeted therapies.