## Assignment 3: Workflow Development and Variant Identification
Assignment Date: Monday, Oct. 11, 2021
Due Date: Monday, Oct. 18, 2021 @ 11:59pm 

WDL workflows require Docker images. For this assignment, you should use this Docker image: [https://github.com/mschatz/wga-essentials](https://github.com/mschatz/wga-essentials)

### Assignment Overview

In this assignment, you will gain familiarity with Workflow Development Language (WDL) and developing an end-to-end variant calling workflow on WDL using [miniwdl](https://github.com/chanzuckerberg/miniwdl).

As a reminder, any questions about the assignment should be posted to [Piazza](https://piazza.com/class/ksxxhnaqr2v6gz).

### Question 1. Hello World [5 pts]

- Using [miniwdl](https://github.com/chanzuckerberg/miniwdl), develop a Hello World workflow that takes in a user's name (`USER_NAME` in string format) and outputs a file saying `Hello, USER_NAME!`. Please submit your code as well as a screenshot of the window in which you run the code. **If you cannot successfully run miniwdl on your local computer, let us know as soon as possible so that we can provide an alternative.**

### Question 2. Identifying a Specific Variant [25 pts]

*Three friends, Ezra, Sabine, and Zeb go out to lunch together and, in discussing the menu, all realize that they all have a specific culinary preference. They believe the cause of this preference to be genetic. Can you identify what SNP causes this preference and what the preference is?*

Download the read set from here: [https://github.com/schatzlab/biomedicalresearch2021/tree/main/assignments/assignment4/input_files](https://github.com/schatzlab/biomedicalresearch2021/tree/main/assignments/assignment4/input_files)

For this question, you may find this tutorial helpful: [http://clavius.bc.edu/~erik/CSHL-advanced-sequencing/freebayes-tutorial.html](http://clavius.bc.edu/~erik/CSHL-advanced-sequencing/freebayes-tutorial.html)

To answer the following questions, use a WDL file to run the required tools. You should use one task per computational question. Please include your WDL file in your submission.

- 2a. You are able to narrow down the SNP to a specific region in chromosome 11. Using BWA-MEM, align their FASTQ files to the provided reference file. How many reads does each file have and how many are successfully mapped? [Hint: Use `samtools flagstat`.]

- 2b. How many SNPs and indels does each file have? [Hint: Sort the SAM file first. Then, call variants with `freebayes`. Summarize using `bcftools stats`.]

- 2c. You now know which SNPs and indels each friend has. However, you want to know which variant they all share. How many variants are shared between all three friends? [Hint: Use `bcftools isec`.]

- 2d. Between the variants shared between all three friends, which is likeliest to cause a phenotype of interest? [Hint: You can search for variants at a certain chromosome and position at https://www.ncbi.nlm.nih.gov/snp/advanced/. Remember, the position in the intersected VCF is the position within the region we're looking at, so you will have to find the starting location of the region!]

- 2e. What is the phenotype? [Hint: Search the name of the gene associated with the variant you found in 2d.]

### Packaging

The solutions to the above questions should be submitted as a single PDF document that includes your name, email address, and all relevant figures (as needed). Make sure to clearly label each of the subproblems and give the exact commands and/or code snippets you used for solving the question. You do not need to show code for plotting. Submit your solutions by uploading the PDF to [GradeScope](https://www.gradescope.com/courses/301857), and remember to select where in your submission each question/subquestion is.

If you submit after this time, you will start to use up your late days. Remember, you are only allowed 96 hours (4 days) for the entire semester!

## Resources

#### [BWA MEM](https://github.com/lh3/bwa) - Short read aligner

```
conda install bwa-mem2
bwa-mem2 index ref.fa
bwa-mem2 mem ref.fa sample.read1.fastq.gz sample.read2.fastq.gz > sample.sam
```

#### [FreeBayes](https://github.com/ekg/freebayes) - Small variant identification

```
conda install freebayes
freebayes -f chr22.fa sample.bam > sample.vcf
```

#### [bcftools](https://samtools.github.io/bcftools/bcftools.html) - VCF summary

```
conda install bcftools
bcftools stats sample.vcf > stats.txt
```

#### [BEDTools](http://bedtools.readthedocs.io/en/latest/) - Genome arithmetic

Get bedtools from conda, if you haven't already.

```
conda install bedtools
```
