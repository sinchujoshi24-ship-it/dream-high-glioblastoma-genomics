# DREAM-High: Computational Glioblastoma Biomarker Development

**Researchers:** Sinchana Joshi and Musfirah Soheil
**Research Program:** DREAM-High  
**Tools:** R, TCGAbiolinks, SummarizedExperiment

## Overview

This project explores whether gene-expression patterns can distinguish primary glioblastoma tumors from normal brain tissue. Using publicly available data from The Cancer Genome Atlas (TCGA), I developed a preliminary 30-gene expression signature and evaluated its ability to separate tumor and normal samples.

## Methods

- Loaded RNA-sequencing data containing 60,660 genes across 391 samples.
- Applied a log2(TPM + 1) transformation to normalize the scale of expression values.
- Compared mean gene expression between 372 primary tumor samples and 5 solid-tissue normal samples. Fourteen recurrent tumor samples were excluded from this comparison.
- Ranked genes by the difference in mean expression between tumor and normal tissue.
- Selected the 15 genes with the largest positive differences and 15 with the largest negative differences.
- Visualized expression patterns using a heatmap and calculated a composite biomarker score from the standardized expression of the 30 selected genes.

## Key Findings

The analysis identified candidate genes with contrasting expression patterns between primary tumors and normal tissue. The 30-gene signature was used to construct a composite score, which was visualized by group using a boxplot.

These findings provide an exploratory framework for investigating gene-expression signatures associated with glioblastoma.

## Figures and Results

- **Gene-expression distribution:** Histogram of tumor-minus-normal expression differences.
- **Expression heatmap:** Patterns across the selected 30 genes in tumor and normal samples.
- **Composite biomarker score:** Boxplot comparing scores between primary tumor and normal samples.

## Limitations

This analysis uses group-mean differences rather than a formal differential-expression significance test. The normal-tissue group contains only five samples, and the selected genes and composite score were evaluated using the same dataset used to develop the signature. Independent validation and more rigorous statistical evaluation are needed before assessing diagnostic performance.

## Research Materials

- [View the R analysis on RPubs](INSERT_YOUR_RPUBS_LINK)
- Research presentation: [Add your presentation link or PDF]

---

*This project represents exploratory computational research and does not establish a clinically validated diagnostic biomarker.*
