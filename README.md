# PC signature from DEGS
### Introduction
Examples of using specific gene set as a principle component signature to integrate with traits in popluation data. 

Targeted experiments can generate specific gene lists and/or pathways which are relevant in the context of a gene or condition (eg. KO vs WT animal or chow vs High-fat Diet).  One question which remains after generating these lists of relevant targets is how specific pathways vary in diverse populations and if this variation is reflected clinically-relevant traits. To address these questions, we took genes of interest from targeted experiments (below) and aggregated into a single vector from global measures of transcript data in a population.  This vector can then be correlated with other parameters or mapped using association to provide a snapshot of these variation of these genes in a population.   

This has been performed  starting from ChIP-Seqgene regions (focus of this example):  

Geoghegan G, Simcox J, Seldin MM, Parnell TJ, Stubben C, Just S, Begaye L, Lusis AJ, Villanueva CJ. Targeted deletion of Tcf7l2 in adipocytes promotes adipocyte hypertrophy and impaired glucose metabolism. Mol Metab. 2019 Jun;24:44-63. doi: 10.1016/j.molmet.2019.03.003. Epub 2019 Mar 14. PubMed PMID: 30948248; PubMed Central PMCID: PMC6531814

As well as Differentially-expressed genes from RNA-Seq:

Yu J, Seldin MM, Fu K, Li S, Lam L, Wang P, Wang Y, Huang D, Nguyen TL, Wei B, Kulkarni RP, Di Carlo D, Teitell M, Pellegrini M, Lusis AJ, Deb A. Topological Arrangement of Cardiac Fibroblasts Regulates Cellular Plasticity. Circ Res. 2018 Jun 22;123(1):73-85. doi: 10.1161/CIRCRESAHA.118.312589. Epub 2018 Apr 24. PubMed PMID: 29691232; PubMed Central PMCID: PMC6014922.


### Steps

In this example, we will use genes ienriched from ChIP-Sequencing peaks which were specific for a targeted (Adipose-sepcific) deletion of Tcf7l2. These genes will be pulled form adipose tissue expression arrays in the Hybrid Mouse Diversity Panel (HMDP) fed a high-fat/high/sucrose diet and correlated with a subset of traits relevant for metabolic disease 

Initially, we will gather these gene sets from population data, perform principle component analysis and ask how variation of each gene "contributes" to the top principle components.

Following this, each HMDP mouse will be assigned a value based on its variation of the principle component genes.  These values will then be used to correlate with clinical traits.  
