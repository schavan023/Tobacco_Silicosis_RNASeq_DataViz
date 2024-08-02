# Silica-Tobacco Smoke Study Report

## Introduction
This study investigates the effects of crystalline silica (CS) and tobacco smoke (TS) on lung toxicity and gene expression profiles in rats. The study focuses on a 6-month exposure (6ME) group to either CS, TS, or a combination of both (CS+TS).

## Objective
The primary objective is to explore the impact of CS and TS, individually and in combination, on lung toxicity and gene expression in rats. Specific goals include:
- **Assess Lung Toxicity:** Examine lung toxicity in rats exposed to different conditions (Control(Air), CS, TS, and CS + TS) over a 6-month period.
- **Analyze Gene Expression Profiles:** Identify differentially expressed genes (DEGs) across the various exposure groups.
- **Perform Bioinformatics Analysis:** Conduct analyses such as PCA, differential expression analysis, pathway enrichment analysis, and GSEA to understand the biological pathways and molecular mechanisms impacted by the exposures.

## Study Design
Male Fischer 344 rats were exposed by inhalation to air, CS (15 mg/m3, 6 h/day, 5 days), TS (80 mg/m3, 3 h/day, twice weekly, 6 months), or CS (15 mg/m3, 6 h/day, 5 days) followed by TS (80 mg/m3, 3 h/day, twice weekly, 6 months). The rats were euthanized 6 months and 3 weeks following initiation of the first exposure and the lung response was assessed.

## Materials and Methods
### Animal Groups and Treatment
Rats were assigned to the following groups and treatments:
- **Control (Air):** Rats 1-6
- **CS:** Rats 13-18
- **TS:** Rats 25-30
- **CS + TS:** Rats 37-42

### Gene Expression Analysis
#### Statistical Analysis
Differential expression analysis was performed using the `limma` package in R. The `voom` function transformed count data for linear modeling, with contrasts defined to compare each treatment group against the control group. Adjusted p-values < 0.05 were considered significant.

### Principal Component Analysis (PCA)
- **Before Normalization:** Initial PCA showed overlap among groups, indicating potential batch effects.
- **After Normalization:** Post-normalization, PCA clearly separated the groups, highlighting the normalization's effectiveness in reducing noise and revealing biological differences.

### Volcano Plots
Volcano plots visualized differential expression results, highlighting genes significantly upregulated or downregulated based on log fold changes and p-values.

### Gene Set Enrichment Analysis (GSEA)
GSEA identified statistically significant differences in gene sets between groups, visualized through dot plots that emphasized the top enriched GO terms.

### KEGG Pathway Enrichment Analysis
Performed using `enrichKEGG` to identify significant biological pathways in the DEGs, providing insights into the biological processes affected by each treatment.

## Results
- Principal Component Analysis (PCA): PCA plots before normalization showed distinct clustering of samples based on their treatment groups, indicating inherent differences in gene expression. PCA plots after normalization demonstrated improved clustering and separation between groups, validating the effectiveness of the normalization process.

- Differential Expression Analysis: We identified significant differentially expressed genes (DEGs) between the exposure groups (CS vs. Air, TS vs. Air, and CS + TS vs. Air). The number of significant DEGs varied across contrasts, reflecting the distinct impact of each exposure condition.

- Volcano Plots: Enhanced volcano plots were used to visualize the DEGs for each contrast. Genes with significant changes in expression were highlighted, providing insights into the molecular alterations caused by CS and TS exposure.

- Gene Set Enrichment Analysis (GSEA):GSEA dot plots revealed key biological pathways enriched in the DEGs for each contrast, highlighting the biological processes affected by the different exposure conditions.

- KEGG Pathway Enrichment Analysis:KEGG pathway enrichment analysis identified significant pathways associated with the DEGs, suggesting potential mechanisms of lung toxicity and disease processes triggered by CS and TS exposure.

## Conclusion
The study enhances our understanding of the pulmonary effects of CS and TS exposure and provides insights into the potential health risks associated with these exposures.

## Publication from which sequence data was used. 
https://academic.oup.com/toxsci/article/178/2/375/5911641
Tina M Sager, Christina M Umbright, Gul Mehnaz Mustafa, Naveena Yanamala, Howard D Leonard, Walter G McKinney, Michael L Kashon, Pius Joseph, Tobacco Smoke Exposure Exacerbated Crystalline Silica-Induced Lung Toxicity in Rats, Toxicological Sciences, Volume 178, Issue 2, December 2020, Pages 375–390, https://doi.org/10.1093/toxsci/kfaa146
