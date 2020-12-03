## FinnSV_paper_1220
The summary statistics of FinMetSeq SV paper

#1.summary statistics for all the SVs detected in WGS data tested against 116 traits
wgs_stats/${trait}.wgs.mac10.txt.gz
The full name of the trait abbreviations can be found from Locke et al. 2020 (PMID:31367044) and Davis et al. 2017 (PMID:29084231) 
Colunms are:
TRAIT - quantitative trait tested
PIPELINE - pipeline used to detect the SV
ID - the ID of SV
CHR - chromosome 
POS - starting point of the SV, in GRCh38 reference
P - p value in discovery phase with WGS data only
BETA - beta in discovery phase with WGS data only
SEBETA - standard deviation of the beta in discovery phase with WGS data only
R2 - R2 in discovery phase with WGS data only
AC - the alternative allele count from WGS data, noted for GenomeSTRiP and CNVnator those are #. alternative copy number carriers
AF - allele frequency 
N - sample size, (sample availability varied by trait)


#2.replication_summary_stats.txt
The summarized table for the replication experiment for the 2053 SV candidates with WGS p<0.001.
Columns are:
ID - SV ID from original pipeline (CNV_chr*_*_* are GenomeSTRiP CNVs, chr*_*_ are CNVnator CNVs, and number IDs belong to LUMPY)
TRAIT - the traits tested for association with (*combined means male and female data combined)
CHR - chromosome
POS - starting point of the SV, in GRCh38 reference
P_WGS - p value in discovery phase with WGS data only
BETA_WGS - beta in discovery phase with WGS data only
AC_WGS - the alternative allele count from WGS data, noted for GenomeSTRiP and CNVnator those are #. alternative copy number carriers
N_WGS - sample size of WGS association tests (sample availability varied by trait) 
P_WES_FE - WES replication meta p value under fixed effects model
BETA_WES_FE - WES replication meta beta under fixed effects model
TOP_EXON - Top exon signal (in hg19 reference)
N_IMP - sample size of imputed SVs' association test (replication phase)
GENOCNT_IMP - count for HOMREF/HET/HOMALT in imputated SV
MAF_IMP - minor allele frequency for imputed SV
P_IMP - replication p value using imputed genotype
BETA_IMP - replication beta using imputed genottype
TYPE - SV type
DR2_IMP - BEAGLE score for imputation quality, an estimated correlation between imputed genotype and real genotype
AF_IMP_CALLSET - allele frequency in the imputed callset
maxR2 - the max genotype correlation with flanking SNPs within 1MB region (calculated by WGS data only)
EXON_R2_BATCH1 - the genotype correlation between WGS detected SV and the exon XHMM-processed read-depth data in batch1 
EXON_R2_BATCH2 - the genotype correlation between WGS detected SV and the exon XHMM-processed read-depth data in batch2
exon_r2_ave - average of the previous two columns
imp_r2_higher - whether the imputation correlation (DR2) is higher than exon_r2_ave
combined_p - combined p values from discovery (P_WGS) and replication (P_IMP or P_WES_FE) using fisher's method

