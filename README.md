# A Resource of Gene Expression Data from a Multiethnic Population Cohort of Induced Pluripotent Cell-Derived Cardiomyocytes

## RNAseq
	

A total of 71 iPSC-CM lines (34 from individuals self-identified as African-Americans and 37 from individuals self-identified as European-Americans; 44 from women, 32 from men) were >=80% positive for troponin T staining (AB-8295, abcam) using flow cytometry. Total RNA was isolated using the RNeasy Mini Kit (QIAGEN) followed by oligo-dT selection. RNA sequencing libraries were prepared using the Illumina TruSeq stranded mRNA kit followed by the Nugen Ovation amplification kit. Libraries were sequenced in 3 batches with an Illumina HiSeq2500 system (performed on a fee-for-service basis by GENEWIZ, Inc.) to a depth of ≈30 million 150-bp paired-end reads per biological sample. FASTQ files were aligned against human reference (hg19/hGRC37) using the STAR aligner. Duplicate reads were removed using MarkDuplicates from Picard tools, and per gene read counts for Ensembl (v75) gene annotations were computed. Expression levels in counts per million (CPM) were normalized and transformed using VOOM in the LIMMA R package. To account for observed batch effects, a surrogate variant analysis was performed using the R package SVAseq and 11 additional covariates were identified. LIMMA was used perform differential gene expression analysis. 

The RNA-seq data and genotype data used to generate this resource are available via the accession numbers GSE146071 and dbGaP: phs001341.v1.p1, respectively.

### Data Download


* [Raw Counts](https://www.dropbox.com/s/okwxf6fxudz5jf2/subread_counts.Rdata?dl=0)
* [SVA Corrected CPMS](https://www.dropbox.com/s/ukg0pmntobs42ge/SVA_corrected_IPCS_CM.RData?dl=0)
* [Final eSet](https://www.dropbox.com/s/06wt0rxx0amypxn/IPSC_CM_final.RData?dl=0)



## eQTL

Expression quantitative trait locus analysis was performed using the QTLtools package with adjustment for sex, race, and the first 3 genetic principal components and the 11 SVA-computed covariates.
