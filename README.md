# EN.601.452 / AS.020.415 Computational Biomedical Research &amp; Advanced Biomedical Research
Prof: [Michael Schatz](http://schatz-lab.org) (mschatz @ cs.jhu.edu) <br>
TA: [Samantha Zarate]() (slzarate @ jhu.edu) <br>
Class Hours: Monday + Wednesday @ 3:00 - 3:50p in Hodson 211 <br>
Schatz Office Hours: By appointment <br>
Zarate Office Hours: TBD and by appointment <br>

**The goal of this course is to prepare undergraduates to understand and perform state-of-the-art biomedical research.** This will be accomplished through three main components: (1) classroom-style lectures on cross cutting techniques for biomedical research focusing on data visualization, statistical inference, and scientific computing; (2) research presentations from distinguished faculty on their active research projects; and (3) a major research project to be performed under the mentorship of a JHU professor. Students will present their research during an in-class symposium at the end of the semester. Grading will be based on homework exercises, a midterm exam, a written research proposal, an interim research report, an oral research presentation, and a final research report.

Within the course, we will study the leading computational and quantitative approaches for comparing and analyzing genomes starting from raw sequencing data. The course will focus on human genomics and human medical applications, but the techniques will be broadly applicable across the tree of life. The topics will include genome assembly & comparative genomics, variant identification & analysis, gene expression & regulation, personal genome analysis, and cancer genomics. There are no formal course prerequisites, although the course will require familiarity with UNIX scripting and/or programming to complete the assignments and course project. 

### Prerequisites
- Online introduction to Unix/Linux. Students are strongly recommended to complete one of the following online tutorials (or both) before class begins. 
  - [Code academy's Intro to Unix](https://www.codecademy.com/en/courses/learn-the-command-line/lessons/environment/exercises/bash-profile)
  - [Rosalind Bioinformatics Programming in Python](http://rosalind.info/problems/locations/)
  - [Minimal Make](http://kbroman.org/minimal_make/)
- Access to a Linux Machine, and/or Install Docker (Unfortuantely, even Mac will not work correctly for some programs)

## Course Resources:
- [Syllabus and Policies](https://github.com/schatzlab/biomedicalresearch2021/tree/master/policies)
- [Piazza Discussion Board](http://piazza.com/jhu/fall2021/en601452)
- [GradeScope](https://www.gradescope.com/courses/301857) Entry Code: D5GDXP
- [Spring 2021 Graduate Course Materials](https://github.com/schatzlab/appliedgenomics2021)

## Related Courses & Readings
- [Applied Comparative Genomics by Aaron Quinlan](https://github.com/quinlan-lab/applied-computational-genomics)
- [Algorithms for DNA Sequencing by Ben Langmead](http://www.langmead-lab.org/teaching-materials/)
- [Computational Biology by Rob Patro](https://rob-p.github.io/CSE549F16/lectures/)
- [HarvardX Biomedical Data Science](http://genomicsclass.github.io/book/)
- [PLOS Computational Biology Translational Bioinformatics](http://collections.plos.org/translational-bioinformatics)
- [Biostars Handbook](https://www.biostarhandbook.com/)

## Related Textbooks
- [Molecular Biology of the Gene (Watson et al)](https://www.amazon.com/Molecular-Biology-Gene-James-Watson/dp/0321762436/ref=pd_lpo_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=R6A5BW06E5RJB7GVSNPY)
- [Molecular Biology of the Cell (Alberts)](http://osp.mans.edu.eg/tmahdy/surgeons/ebooks/Books/Alberts%20-%20Molecular%20Biology%20of%20the%20Cell.pdf)
- [Biological Sequence Analysis (Durbin et al)](https://www.amazon.com/Biological-Sequence-Analysis-Probabilistic-Proteins/dp/0521629713)
- [Modern Statistics for Modern Biology (Holmes & Huber)](https://www.huber.embl.de/msmb/index.html)

## Schedule
| # | Date | Lecture | Readings & Resources | Assignment |
|:--|:-----|:--------|:---------------------|:-----------|
|1.  | Mo 1/25 | Introduction | * [Biological data sciences in genome research (Schatz, 2015, Genome Research)](http://genome.cshlp.org/content/25/10/1417.full) <br> * [Big Data: Astronomical or Genomical? (Stephens et al, 2015, PLOS Biology)](http://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1002195) | [Sign Up for Piazza](https://piazza.com/class/ksxxhnaqr2v6gz) |
|2.  | We 1/27 | Genomic Technologies | * [Molecular Structure of Nucleic Acid (Watson and Crick, 1953, Nature)](http://www.nature.com/nature/dna50/watsoncrick.pdf) <br> * [Coming of age: ten years of next-generation sequencing technologies (Goodwin et al, 2016, Nature Reviews Genetics)](http://www.nature.com/nrg/journal/v17/n6/full/nrg.2016.49.html) <br> * [Piercing the dark matter: bioinformatics of long-range sequencing and mapping (Sedlazeck et al, 2018, Nature Reviews Genetics)](https://www.nature.com/articles/s41576-018-0003-4)| [Assignment 1](https://github.com/schatzlab/appliedgenomics2021/blob/master/assignments/assignment1/README.md)
|3.  | Mo 2/1  | Whole Genome Assembly | * [Velvet: Algorithms for de novo short read assembly using de Bruijn graphs (Zerbino and Birney, 2008, Genome Research)](http://genome.cshlp.org/content/18/5/821.full) <br> * [Quake: quality-aware detection and correction of sequencing errors (Kelley et al, 2010, Genome Biology)](http://genomebiology.biomedcentral.com/articles/10.1186/gb-2010-11-11-r116) <br> * [Allpaths-LG: High-quality draft assemblies of mammalian genomes from massively parallel sequence data (Gnerre et al, 2011, PNAS)](http://www.pnas.org/content/108/4/1513) <br> * [FALCON-unzip: Phased diploid genome assembly with single-molecule real-time sequencing (Chin et al, 2016, Nature Methods)](http://www.nature.com/nmeth/journal/v13/n12/full/nmeth.4035.html) <br>  | 
|4.  | We 2/3  | Whole Genome Assembly and Alignment | * [Toward simplifying and accurately formulating fragment assembly. (Myers, 1995, J. Comp. Bio.)](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.52.6330&rep=rep1&type=pdf) <br> * [MHAP: Assembling large genomes with single-molecule sequencing and locality-sensitive hashing (Berlin et al, 2015, Nature Biotech)](http://www.nature.com/nbt/journal/v33/n6/abs/nbt.3238.html) <br> * [Genome assembly forensics: finding the elusive mis-assembly (Phillippy et al, 2008, Genome Biology)](http://genomebiology.biomedcentral.com/articles/10.1186/gb-2008-9-3-r55) <br> * [MUMmer: Alignment of Whole Genomes (Delcher et al, 1999, NAR)](http://mummer.sourceforge.net/MUMmer.pdf) | [Assignment 2](https://github.com/schatzlab/appliedgenomics2021/blob/master/assignments/assignment2/README.md)
|5.  | Mo 2/8 | The human genome and intro to long reads | * [Piercing the dark matter: bioinformatics of long- range sequencing and mapping (Sedlazeck et al, 2018, Nature Reviews Genetics)](https://www.nature.com/articles/s41576-018-0003-4) <br> * [Nanopore sequencing and assembly of a human genome with ultra-long reads (Jain et al, 2018, Nature Biotech)](https://www.nature.com/articles/nbt.4060) |
|6.  | We 2/10 | Variant Analysis | * [Haplotype-based variant detection from short-read sequencing (Garrison and Marth, arXiv, 2012)](https://arxiv.org/abs/1207.3907) <br> * [The Genome Analysis Toolkit: A MapReduce framework for analyzing next-generation DNA sequencing data (McKenna et al, 2010, Genome Research)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2928508/) <br> * [A universal SNP and small-indel variant caller using deep neural networks (Poplin et al, 2018, Nature Biotechnology](https://www.nature.com/articles/nbt.4235) <br> * [SAM/BAM/Samtools: The Sequence Alignment/Map format and SAMtools (Li et al, 2009, Bioinformatics)](https://academic.oup.com/bioinformatics/article/25/16/2078/204688/The-Sequence-Alignment-Map-format-and-SAMtools) <br> * [IGV: Integrative genomics viewer (Robinson et al, 2011, Nature Biotech)](http://www.nature.com/nbt/journal/v29/n1/full/nbt.1754.html) | [Assignment 3](https://github.com/schatzlab/appliedgenomics2021/blob/master/assignments/assignment3/README.md)
|7. | Mo 2/15 | Genome Arithmetic and Plane Sweep | * [BEDTools: a flexible suite of utilities for comparing genomic features (Quinlan & Hall, 2010, Bioinformatics)](https://academic.oup.com/bioinformatics/article/26/6/841/244688/BEDTools-a-flexible-suite-of-utilities-for) <br> * [A Parallel Algorithm for N-Way Interval Set Intersection (Layer & Quinlan, 2016, IEEE Proceedings)](http://ieeexplore.ieee.org/document/7289350/?tp=&arnumber=7289350&url=http:%2F%2Fieeexplore.ieee.org%2Fiel7%2F5%2F4357935%2F07289350.pdf%3Farnumber%3D7289350) |
|8.  | We 2/17 | Machine Learning Primer | * [What are decision trees? (Kingsford and Salzberg, 2008, Nature Biotechnology)](https://www.nature.com/articles/nbt0908-1011.pdf?origin=ppub) <br> * [What is a hidden Markov model? (Eddy, 2004, Nature Biotechnology)](http://www.nature.com/nbt/journal/v22/n10/full/nbt1004-1315.html) <br> * [Deep learning in biomedicine (Wainberg et al, 2018, Nature Biotechnology)](https://www.nature.com/articles/nbt.4233) <br> * [Visualizing Data Using t-SNE](https://www.youtube.com/watch?v=RJVL80Gg3lA) | [Assignment 4](https://github.com/schatzlab/appliedgenomics2021/blob/master/assignments/assignment4/README.md)
|9.  | Mo 2/22 | Structural Variant Analysis | * [Accurate detection of complex structural variations using single-molecule sequencing (Sedlazeck et al, 2018, Nature Methods)](https://www.nature.com/articles/s41592-018-0001-7) <br> * [Characterizing the Major Structural Variant Alleles of the Human Genome (Audano et al, 2019, Cell)](https://www.cell.com/cell/pdf/S0092-8674(18)31633-7.pdf) <br> * [Resolving the complexity of the human genome using single-molecule sequencing (Chaisson et al, 2015, Nature)](http://www.nature.com/nature/journal/v517/n7536/abs/nature13907.html) 
|10. | We 2/24 | Read Mapping | * [How to map billions of short reads onto genomes (Trapnell and Salzberg, 2009, Nature Biotech)](http://www.nature.com/nbt/journal/v27/n5/full/nbt0509-455.html) <br> * [Bowtie: Ultrafast and memory-efficient alignment of short DNA sequences to the human genome (Langmead et al, 2009, Genome Biology)](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2009-10-3-r25) <br> * [BWA-MEM: Aligning sequence reads, clone sequences and assembly contigs with BWA-MEM (Li, 2013, arXiv)](https://arxiv.org/abs/1303.3997) <br> * [Sapling: Accelerating Suffix Array Queries with Learned Data Models (Kirsche et al, 2020, bioRxiv](https://www.biorxiv.org/content/10.1101/2020.01.29.925768v1.full) | 
|11. | Mo 3/1  | Nanopore Signal Analysis | * [Targeted nanopore sequencing by real-time mapping of raw electrical signal with UNCALLED (Kovaka et al, 2020, bioRxiv)](https://www.biorxiv.org/content/10.1101/2020.02.03.931923v1) <br> * [Detecting DNA cytosine methylation using nanopore sequencing (Simpson et al, 2017, Nature Methods)](https://www.nature.com/articles/nmeth.4184)
|12. | We 3/3 | Functional Analysis 1: Annotation | * [BLAST: Basic Local Alignment Search Tool](http://s3.amazonaws.com/academia.edu.documents/25023760/altschul1990.pdf?AWSAccessKeyId=AKIAIWOWYYGZ2Y53UL3A&Expires=1488914265&Signature=zX6z9PyBMXesvcCdR3PTHVO%2BtFU%3D&response-content-disposition=inline%3B%20filename%3DBasic_local_alignment_search_tool.pdf) <br> * [Glimmer: Microbial gene identification using interpolated Markov models](http://www.cs.jhu.edu/~genomics/Glimmer/glimmer-nar.pdf) <br> * [MAKER2: an annotation pipeline and genome-database management tool for second-generation genome projects](http://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-491) <br>  | [Assignment 5](https://github.com/schatzlab/appliedgenomics2021/blob/master/assignments/assignment5/README.md)
|13. | Mo 3/8  | Functional Analysis 2: RNA-seq | * [RNA-Seq: a revolutionary tool for transcriptomics (Wang et al, 2009. Nature Reviews Genetics)](http://www.nature.com/nrg/journal/v10/n1/full/nrg2484.html)<br> * [Differential gene and transcript expression analysis of RNA-seq experiments with TopHat and Cufflinks (Trapnell et al, 2012, Nature Protocols)](http://www.nature.com/nprot/journal/v7/n3/full/nprot.2012.016.html)<br> * [Salmon provides fast and bias-aware quantification of transcript expression (Patro et al, 2017, Nature Methods)](http://www.nature.com/nmeth/journal/vaop/ncurrent/full/nmeth.4197.html)<br> * [Bismark: a flexible aligner and methylation caller for Bisulfite-Seq applications (Krueger and Andrews, 2011, Bioinformatics)](https://academic.oup.com/bioinformatics/article/27/11/1571/216956/Bismark-a-flexible-aligner-and-methylation-caller) | [Project Proposal](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/proposal.md)
|14. | We 3/10 | Functional Analysis 3: Methyl-seq, Chip-seq, and Hi-C | * [ChIP–seq and beyond: new and improved methodologies to detect and characterize protein–DNA interactions (Furey, 2012, Nature Reviews Genetics)](http://www.nature.com/nrg/journal/v13/n12/abs/nrg3306.html)<br> * [PeakSeq enables systematic scoring of ChIP-seq experiments relative to controls (Rozowsky et al. 2009. Nature Biotech)](http://www.nature.com/nbt/journal/v27/n1/full/nbt.1518.html) <br> * [Comprehensive Mapping of Long-Range Interactions Reveals Folding Principles of the Human Genome (Lieberman-Aiden et al, 2009, Science)](http://science.sciencemag.org/content/326/5950/289) | 
|15. | Mo 3/15 | Functional Analysis 4: Regulatory States, ENCODE, GTEx, RoadMap | * [An integrated encyclopedia of DNA elements in the human genome (The ENCODE Project Consortium, Nature, 2012)](http://www.nature.com/nature/journal/v489/n7414/full/nature11247.html) <br> * [Genetic effects on gene expression across human tissues (GTEx Consortium, Nature, 2017)](https://www.nature.com/articles/nature24277) <br> * [Integrative analysis of 111 reference human epigenomes (Roadmap Epigenome Consortium, Nature, 2015)](https://www.nature.com/articles/nature14248) <br> * [ChromHMM: automating chromatin-state discovery and characterization (Ernst & Kellis, 2012, Nature Methods)](http://www.nature.com/nmeth/journal/v9/n3/full/nmeth.1906.html) <br> * [Segway: Unsupervised pattern discovery in human chromatin structure through genomic segmentation (Hoffman et al, 2012, Nature Methods)](http://www.nature.com/nmeth/journal/v9/n5/full/nmeth.1937.html) | 
|16. | We 3/17| Functional Analysis 5: Single Cell Genomics | * [Ginkgo: Interactive analysis and assessment of single-cell copy-number variations (Garvin et al, 2015, Nature Methods)](http://www.nature.com/nmeth/journal/v12/n11/full/nmeth.3578.html) <br> * [The dynamics and regulators of cell fate decisions are revealed by pseudotemporal ordering of single cells (Trapnell et al, Nature Biotech, 2014)](https://www.nature.com/articles/nbt.2859) <br> * [Eleven grand challenges in single-cell data science (Lähnemann et al, Genome Biology, 2020)](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-020-1926-6)  | 
|* | Mo 3/22 | Spring Break! | |
|17. | We 3/24  | Midterm Review | | [Preliminary Project Report](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/prelimreport.md)
|18. | Mo 3/29  | Midterm Exam | | *Take home exam*
|19. | We 3/31  | Human Evolution | * [An integrated map of genetic variation from 1,092 human genomes (1000 Genomes Consortium, 2012, Nature)](http://www.nature.com/nature/journal/v491/n7422/full/nature11632.html) <br> * [Analysis of protein-coding genetic variation in 60,706 humans (Let et al, 2016, Nature)](http://www.nature.com/nature/journal/v536/n7616/full/nature19057.html) <br> * [A Draft Sequence of the Neandertal Genome (Green et al. 2010, Science)](http://science.sciencemag.org/content/328/5979/710.full) <br> * [Excavating Neandertal and Denisovan DNA from the genomes of Melanesian individuals (Vernot et al. 2016. Science)](http://science.sciencemag.org/content/early/2016/03/16/science.aad9416.full) | 
|20. | Mo 4/5 | Human Genetic Diseases | * [Genome-Wide Association Studies (Bush & Moore, 2012, PLOS Comp Bio)](https://doi.org/10.1371/journal.pcbi.1002822) <br> * [The contribution of de novo coding mutations to autism spectrum disorder (Iossifov et al, 2014, Nature)](https://www.nature.com/nature/journal/v515/n7526/full/nature13908.html)
|21. | We 4/7 | Cancer Genomics | * [The Hallmarks of Cancer (Hanahan & Weinberg, 2000, Cell)](http://www.sciencedirect.com/science/article/pii/S0092867400816839) <br> * [Evolution of Cancer Genomes (Yates & Campbell, 2012, Nature Reviews Genetics)](http://www.nature.com/nrg/journal/v13/n11/full/nrg3317.html) <br> * [Comprehensive molecular portraits of human breast tumours (TCGA, 2012, Nature)](http://www.nature.com/nature/journal/v490/n7418/full/nature11412.html) | [Project Presentations](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/presentations.md)
|22. | Mo 4/12 | Microbiome and Metagenomics | * [Kraken: ultrafast metagenomic sequence classification using exact alignments (Wood and Salzberg, 2014, Genome Biology)](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2014-15-3-r46) <br> * [Chapter 12: Human Microbiome Analysis (Morgan and Huttenhower)](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1002808) | 
|* | We 4/14 | Spring Break! | |
|23. | Mo 4/19 | Genomic Futures | * ["Snyderome" Personal Omics Profiling Reveals Dynamic Molecular and Medical Phenotypes (Chen et al, 2012, Cell)](http://www.sciencedirect.com/science/article/pii/S0092867412001663) <br> * [Identifying Personal Genomes by Surname Inference (Gymrek et al, 2013, Science)](http://science.sciencemag.org/content/339/6117/321) | [Project Report](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/finalreport.md)
|24. | We 4/21 | [Project Presentations](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/presentations.md) | | 
|25. | Mo 4/26 | [Project Presentations](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/presentations.md) | | 
|26. | We 4/28 | [Project Presentations](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/presentations.md) | | 
| | Wed 5/12 | [Final Project Report Due!](https://github.com/schatzlab/appliedgenomics2021/blob/master/project/finalreport.md)| | 



