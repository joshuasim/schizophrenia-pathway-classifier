# Schizophrenia Pathway Classification
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![GSEApy](https://img.shields.io/badge/GSEApy-latest-orange)
![Status](https://img.shields.io/badge/Status-In_Progress-orange)

Primary Question: Will immune/inflammatory pathway genes, implicated in schizophrenia by independent studies, show enrichment in expression differences between SCZ vs. control subjects in GSE21138 dataset, and will a classifier trained on this expression data learn features reflecting this signal?

Secondary/Exploratory Question: Are the classifier's learned features aligned more closely with long-term-illness or short-term-illness signatures reported in GSE21138's original study?

---

## Introduction/Motivation

Schizophrenia is a debilitating mental disorder that is one of the leading causes of disability in the world, causing disruptions in thought process, perception, emotional responsiveness, and social interactions (NIMH, n.d.). 

Many studies have been conducted to understand the causative pathophysiology and genetic link to schizophrenia, and while genome-wide association studies (GWAS) have identified distinct, individual genetic variations that contribute to increased susceptibility for developing the disorder, the exact effect of these genes — and how they cause the disorder — is still not fully understood. "The functional characterization and neurobiological import of these loci remain to be elucidated" (Birnbaum & Weinberger, 2017). 

Given this gap in understanding what identified gene variants involved in the disorder actually do to the brain, the seemingly obvious next step would be narrowing in further on individual gene variants. However, research has instead increasingly recognized that schizophrenia has an intricate polygenic nature, with risk spread across many alleles scattered throughout the genome that each have a combined effect on overall disease susceptibility (Schizophrenia Working Group of the PGC, 2014). This suggests that biological pathways, rather than individual genes, might be a better lens for understanding — and eventually diagnosing — schizophrenia. 

Through my own literature review, I noticed two recurring patterns that showed up across different papers. The first was that individual genes tend not to replicate, both within a single study and across independent ones. In its own PCR validation, the paper behind the main dataset used in this project, "Molecular Profiles of Schizophrenia in the CNS at Different Stages of Illness" (Narayan et al., 2008), tested 12 transcripts and found that only 4 genes (SAMSN1, CDC42BPB, DSC2, and PTPRE) held up consistently across the three different illness-duration subgroups it examined — showing weak replication even within its own cohort. This issue of weak replication is not unique to this one study. In a 2019 postmortem comparison of schizophrenia, bipolar disorder, and major depressive disorder, the study points out that more than a decade of RNA profiling work in this field has run into consistent trouble replicating individual-gene findings across different study cohorts, due to a mix of technical and biological factors (Lanz et al., 2019). A more recent review of postmortem transcriptomics offers a possible reason as to why this is the case: these transcriptional changes are cell-type specific and vary significantly for different individuals, which makes single-gene findings hard to reproduce (Ruzicka & Subburaju, 2026). 

The second pattern I noticed through my literature review was that, despite this lack of consistency at the individual gene level, immune and inflammatory pathways kept showing up across independent studies even when using different methods. A 2017 meta-analysis of postmortem brain studies found increased microglial — specialized immune cells — density in schizophrenia patients compared to controls, along with a rise in pro-inflammatory gene activity measured at both the transcript and protein level (van Kesteren et al., 2017). Similarly, the 2019 study on postmortem comparison of schizophrenia, bipolar disorder, and major depressive disorder referenced earlier found that schizophrenia patients — not those with bipolar disorder or major depressive disorder — had more inflammation-linked transcripts turned on across several brain regions, a finding later confirmed with additional lab testing. Using machine learning applied to gene expression data pooled from five independent datasets, a 2025 study found that the genes distinguishing schizophrenia samples were disproportionately tied to immune-system activity (Weng et al., 2025). At the genetic level, one of the largest schizophrenia GWAS studies to date found that risk-associated genes were unusually active in tissues connected to the immune system — genetic support for a link researchers had suspected (Schizophrenia Working Group of the PGC, 2014). Even within the main dataset this project uses, the paper behind the GSE21138 dataset found that long-term illness specifically was associated with inflammation, stimulus-response, and immune function (Narayan et al., 2008). 

Not every study I looked at found this pattern though — a transcriptome-wide pathway analysis of the superior temporal cortex (BA22) found dysregulation centered on synaptic plasticity rather than immune or inflammatory pathways, meaning this pattern I am testing is not a foregone conclusion (Barnes et al., 2011). 

Recognizing this pattern of consistent overlap of immune and inflammatory pathways appearing across independent studies even when individual genes fail to replicate led me to develop my primary hypothesis: Will immune/inflammatory pathway genes, implicated in schizophrenia by independent studies, show enrichment in expression differences between SCZ vs. control subjects in the GSE21138 dataset, and will a classifier trained on this expression data learn features reflecting this signal? To test whether this signal holds independent of the GSE21138 dataset's own duration-based framing, I also developed a secondary, exploratory hypothesis: Are the classifier's learned features aligned more closely with long-term-illness or short-term-illness signatures reported in GSE21138's original study? 

--- 

## Dataset

**Source:** [GSE21138]

---

## Methods

EDA -> enrichment analysis -> classifier construction -> interpret features
---

## Results


---

## Conclusion/Limitations


---

## Reproduction Instructions


---

## References 

Barnes, M. R. et al. (2011). Transcription and pathway analysis of the superior temporal cortex and anterior prefrontal cortex in schizophrenia. Journal of Neuroscience Research, 89(9), 1218–1227. https://pubmed.ncbi.nlm.nih.gov/21538462/

Birnbaum, R., & Weinberger, D. R. (2017). Genetic insights into the neurodevelopmental origins of schizophrenia. Nature Reviews Neuroscience, 18(12), 727–740. https://www.nature.com/articles/nrn.2017.125

Lanz, T. A., Reinhart, V., Sheehan, M. J., Sukoff Rizzo, S. J., Bove, S. E., James, L. C., Volfson, D., Lewis, D. A., & Kleiman, R. J. (2019). Postmortem transcriptional profiling reveals widespread increase in inflammation in schizophrenia. Translational Psychiatry, 9, 151. https://www.nature.com/articles/s41398-019-0492-8

Narayan, S., Tang, B., Head, S. R., Gilmartin, T. J., Sutcliffe, J. G., Dean, B., & Thomas, E. A. (2008). Molecular profiles of schizophrenia in the CNS at different stages of illness. Brain Research, 1239, 235–248. https://pubmed.ncbi.nlm.nih.gov/18778695/

National Institute of Mental Health (NIMH). Schizophrenia. Retrieved from https://www.nimh.nih.gov/health/statistics/schizophrenia

Ruzicka, W. B., & Subburaju, S. (2026). Decoding schizophrenia through postmortem human brain transcriptomics. Current Opinion in Genetics & Development, 97, 102434. https://doi.org/10.1016/j.gde.2026.102434

Schizophrenia Working Group of the Psychiatric Genomics Consortium. (2014). Biological insights from 108 schizophrenia-associated genetic loci. Nature, 511, 421–427. https://www.nature.com/articles/nature13595

van Kesteren, C. F. M. G., Gremmels, H., de Witte, L. D., Hol, E. M., Van Gool, A. R., Falkai, P. G., Kahn, R. S., & Sommer, I. E. (2017). Immune involvement in the pathogenesis of schizophrenia: a meta-analysis on postmortem brain studies. Translational Psychiatry, 7, e1075. https://pubmed.ncbi.nlm.nih.gov/28350400/

Weng, J., Zhu, X., Ouyang, Y., Liu, Y., Lu, H., Yao, J., et al. (2025). Identification of immune-related biomarkers of schizophrenia in the central nervous system using bioinformatic methods and machine learning algorithms. Molecular Neurobiology, 62, 3226–3243. https://link.springer.com/article/10.1007/s12035-024-04461-5
