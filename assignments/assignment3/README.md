## Assignment 3: Variant Analysis and Mappability
Assignment Date: Monday, Sept. 27, 2021 <br>
Due Date: Monday, Oct. 4, 2021 @ 11:59pm <br>

Some of the tools you will need to use only run in a Unix environemnt. For this, you should use Docker. This Docker instance has these tools preinstalled: [https://github.com/mschatz/wga-essentials](https://github.com/mschatz/wga-essentials)

### Assignment Overview

In this assignment, you will take a look at mappability, get some experience with small variant analysis, and analyze some variant data.

For questions 1 and 2 of this assignment, you will be using chromosome 22 from build 38 of the human genome - download it here: [http://hgdownload.cse.ucsc.edu/goldenPath/hg38/chromosomes/chr22.fa.gz](http://hgdownload.cse.ucsc.edu/goldenPath/hg38/chromosomes/chr22.fa.gz). Whenever we refer to chromosome 22 in this assignment, this is what you should use.

As a reminder, any questions about the assignment should be posted to [Piazza](https://piazza.com/class/ksxxhnaqr2v6gz).

### Question 1. Mappability Analysis [15 pts]

- 1a. Using k = 100, extract every k-mer from chromosome 22, and align them back to chromosome 22 using bowtie2. How many 100-mers are mapped back to the correct position (the place they were extracted from) with mapq >= 20? How many are mapped with mapq >= 20, but to an incorrect position?

- 1b. We consider k-mers that are mapped back to their correct position in the genome with mapq >= 20 to be uniquely mappable. For each position in chromosome 22, count how many uniquely mappable k-mers are mapped to it. Make a histogram of the number of positions in chromosome 22 with a given number of uniquely mappable k-mers overlapping them. Use k = 100, and the 100-mers you generated in 1a. [Hint: What is the maximum number of k-mers that can uniquely map to a single position? How many 100-mers can overlap one base in chromosome 22?]

- 1c. Repeat the previous two questions for k = 25, 50 and 200, and discuss (in a couple of sentences) the effect of k on how many k-mers are uniquely mappable and on how many uniquely mappable k-mers overlap each position in the genome.

### Question 2. Small Variant Analysis [10 pts]

Download the read set from here: [http://schatzlab.cshl.edu/data/teaching/sample.tgz](http://schatzlab.cshl.edu/data/teaching/sample.tgz)

For this question, you may find this tutorial helpful: [http://clavius.bc.edu/~erik/CSHL-advanced-sequencing/freebayes-tutorial.html](http://clavius.bc.edu/~erik/CSHL-advanced-sequencing/freebayes-tutorial.html)

- 2a. Using bowtie2, how many reads align to the chromosome 22 reference? How many reads did not align? How many aligned reads had a mate that did not align (AKA singletons)? Count each read in a pair separately. [Hint: Build the index using `bowtie2-build`, align reads using `bowtie2`, analyze with `samtools flagstat`.]

- 2b. How many reads are mapped to the reverse strand? Count each read in a pair separately. [Hint: Find out what SAM flags mean [here](https://broadinstitute.github.io/picard/explain-flags.html) and use `samtools view`.]

- 2c. How many high-quality (QUAL > 20) single nucleotide and indel variants does the sample have? Of the indels, how many are insertions and how many are deletions? [Hint: Identify variants using `freebayes` - sort the SAM file first. Then call variants with `freebayes`. Filter using `bcftools filter`, and summarize using `bcftools stats`.]


### Question 3. Binomial Distribution [10 pts]

- 3a. For coverage n = 10 to 200, calculate the maximum number of minor allele reads (round down) that would make your one-sided binomial test reject the null hypothesis p=0.5 at 0.05 significance. Plot coverage on the x-axis and (number of reads)/(coverage) on the y-axis. Note this is the minimum number of reads that are necessary to believe we might have a heterozygous variant on the second haplotype rather than just mere sequencing error.

- 3b. What asymptote does the plot seem to approach? Why is this?

### Packaging

The solutions to the above questions should be submitted as a single PDF document that includes your name, email address, and all relevant figures (as needed). Make sure to clearly label each of the subproblems and give the exact commands and/or code snippets you used for solving the question. You do not need to show code for plotting. Submit your solutions by uploading the PDF to [GradeScope](https://www.gradescope.com/courses/301857), and remember to select where in your submission each question/subquestion is.

If you submit after this time, you will start to use up your late days. Remember, you are only allowed 96 hours (4 days) for the entire semester!

## Resources

#### [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml) - Short read aligner

```
conda install bowtie2
bowtie2-build chr22.fa chr22
bowtie2 -x chr22 -1 sample/pair.1.fq -2 sample/pair.2.fq > sample.sam
```

While running alignments, if you get an error `Warning: Exhausted best-first chunk memory for read XXXX; skipping read` increase the command-line parameter `--chunkmbs`.

#### [FreeBayes](https://github.com/ekg/freebayes) - Small variant identification

```
conda install freebayes
freebayes -f chr22.fa sample.bam > sample.vcf
```

#### [bcftools](https://samtools.github.io/bcftools/bcftools.html) - VCF summary

```
conda install bcftools
bcftools filter -e "QUAL<20" sample.vcf > filtered.vcf
bcftools stats filtered.vcf > stats.txt
```


#### [BEDTools](http://bedtools.readthedocs.io/en/latest/) - Genome arithmetic

Get bedtools from conda, if you haven't already.

```
conda install bedtools
```
