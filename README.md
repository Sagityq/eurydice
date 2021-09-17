**2021/09/17 - [[WARNING]] THIS WORKFLOW IS UNDER ACTIVE DEVELOPMENT--**
**USE AT OWN DISCRETION**

<h1>eurydice: RNA-seq variant calling (GATK)</h1>

<p align="center">
<img src="img/eurydice_schema.svg">
</p>

**eurydice** is an RNA-seq pipeline that identifies short variants (SNPs and 
indels) from raw sequencing data.The current implementation of
[GATK](https://gatk.broadinstitute.org/hc/en-us/articles/360035531192-RNAseq-short-variant-discovery-SNPs-Indels-)
workflows does not support the joint calling of RNA-seq to operate on a set of 
samples in parallel. This issue, compounded with inherently long runtimes for 
GATK tools such as
[HaplotypeCaller](https://gatk.broadinstitute.org/hc/en-us/articles/360037225632-HaplotypeCaller),
present a challenge in processing the data efficiently in terms of time and 
resources. **eurydice** was developed with consideration of GATK best practices 
for variant calling of RNA-seq data and to be scalable on both the sample- and 
chromosomal-level.

In-depth explanation of the workflow steps, file structure, benchmarking, 
rationale for software and techniques chosen, and other information 
may be found on the **eurydice** entry at the 
[Data Science DokuWiki](https://hpc.agios.local/dokuwiki/doku.php?id=eurydice_gatk_variant_calling).