# Project Ideas

Here are a few selected projects organized by theme, although you are also free to present your own project ideas. A good project is one that:
 
  1. Has a well defined goal
  2. Has a well defined method proposed for solving it; and 
  3. Has appropriate data and resources available. 
 
If any of these are not available, your project will not be successful, especially in the limited time remaining for class. A successful model for the class project is to apply a technique developed in a different context to the biological problem of your choice. Another successful model is to identify an important paper of interest and then try to improve apon their method in some way (faster, less memory, more sensitive, more precise, novel species, novel data sets, etc).

## T2T-based analysis: [T2T-main](https://www.biorxiv.org/content/10.1101/2021.05.26.445798v1) and [T2T-variants](https://www.biorxiv.org/content/10.1101/2021.07.12.452063v1)

1. Short-read structural variant analysis: Use [Parliament2](https://academic.oup.com/gigascience/article/9/12/giaa145/6042728) to call SVs in some of the 1000 genomes samples. Compare the result using GRCh38 to CHM13 and compare short and long read SV calls.

2. Evaluate DeepVariant with CHM13 using short read data from a few samples. Compare to both GRCh38 and CHM13, and compare DeepVariant to GATK results. Investigate the regions that show the largest differences

3. Evaluate exome sequencing with the CHM13 genome by aligning several samples to both GRCh38 and CHM13. Include a few samples that also have whole genome data available.

4. RNA-seq analysis: Use [StringTie2](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1910-1) to analyze short read RNAseq data. Align the reads to
both GRCh38 and CHM13 and investigate differences. RNAseq reads are available from [(Lappalainen et al, 2013, Nature)](https://www.nature.com/articles/nature12531). Stretch
goal is to investigate eQTLs

5. Functional genomics analysis: Apply [Basenji](https://genome.cshlp.org/content/28/5/739.full) to both GRCh38 and CHM13 and compare results. If needed, focus on one
chromosome


## CS Theory and Systems

1. Adapt one or more learned data structures for genomics data:
[Learned Data Structures](https://arxiv.org/abs/1712.01208)

2. Accelerate an important genomics pipeline using GPUs or cloud computing and use that to study a larger dataset
[Rail-RNA](https://academic.oup.com/bioinformatics/article-abstract/doi/10.1093/bioinformatics/btw575/2525684/Rail-RNA-Scalable-analysis-of-RNA-seq-splicing-and)

3. Implement a genomics processing pipeline using WebAssembly and/or Objective-C/Swift/Android [fastq.bio](https://www.smashingmagazine.com/2019/04/webassembly-speed-web-app/)

4. Develop a novel visualization of genomics data (especially from 23-and-me reports or single cell data):
[Circos](http://genome.cshlp.org/content/19/9/1639.full)

5. Apply deep learning techniques to a problem in genomics
[Primer](https://www.nature.com/articles/s41588-018-0295-5)

6. Develop a novel fastq/BAM compression scheme for long term storage (which may require a large precomputed dictionary and/or extensive compute)


## Or your own idea! 

This should be more than you are already doing, but can be a novel twist to a dataset/idea you are already using. If you have a research idea but not the right data, let me know and I'll help you find some.
