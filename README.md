# Study of ColE1 expression using public data

## Finding relevant data in short read archive

We searched [NCBI SRA](https://www.ncbi.nlm.nih.gov/sra) with the following query:

```
(((("escherichia coli"[Organism]) 
  AND "illumina"[Platform]) 
  AND "transcriptomic"[Source]) 
  AND "rna seq"[Strategy]) 
  AND ("2018"[Publication Date] : "2019"[Publication Date]) 
```

## Possible good hit: https://www.ncbi.nlm.nih.gov/bioproject/PRJNA459526

This contaions 16 datasets. We downloaded RunInfo table from NCBI and removed columns to produce this:

```
SRR7119574	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119574	lacZ_ind_RPF_r2
SRR7119575	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119575	lacZ_ind_mRNA_r2
SRR7119576	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119576	lacZ_unind_RPF_r2
SRR7119577	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119577	lacZ_unind_mRNA_r2
SRR7119562	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119562	lacZ_ind_RPF_r1
SRR7119563	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119563	lacZ_ind_mRNA_r1
SRR7119572	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119572	lacZ_unind_RPF_r1
SRR7119573	https://sra-download.ncbi.nlm.nih.gov/traces/sra62/SRR/006952/SRR7119573	lacZ_unind_mRNA_r1
```

## Read processing 

The reads contain the following adapaters:

```
-a TGGAATTCTCGGGTGCCAAGGAACTCCAGTCACGCCAATATCTCGTATGCCGTCTTCTGCTTG 
-b TGGAATTCTCGGGTGCCAAGGAACTCCAGTCACGCCAATATCTCGTATGCCGTCTTCTGCTTG 
-g AATGATACGGCGACCACCGACAGGTTCAGAGTTCTACAGTCCGACGA
```



