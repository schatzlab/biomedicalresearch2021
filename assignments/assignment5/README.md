## Assignment 5: RNA-seq
Assignment Date: Monday, Oct. 25, 2021 <br>
Due Date: Monday, Nov. 1, 2021 @ 11:59pm <br>

### Assignment Overview

In this assignment, you will explore a couple of aspects of RNA-seq (with a small introduction to clustering). For this assignment, you will have to generate some visualizations - we recommend R or Python, but use a language you are comfortable with! 

**Make sure to show your work/code in your writeup!**

As a reminder, post any questions about this assignment to [Piazza](https://piazza.com/class/ksxxhnaqr2v6gz).

#### Question 1. Time Series [20 pts]

[This file](http://schatz-lab.org/teaching/exercises/rnaseq/rnaseq.1.expression/expression.txt) contains normalized expression
values for 100 genes over 10 time points. Most genes have a stable background expression level, but some special genes show increased
expression over the time course and some show decreased expression.

- Question 1a. Cluster the genes using an algorithm of your choice. Which genes show increasing expression and which genes show decreasing expression, and how did you determine this? What is the background expression level (numerical value) and how did you determine this?
[Hint: K-means and hierarchical clustering are common clustering algorithms you could try.]

- Question 1b. Calculate the first two principal components of the expression matrix. Show the plot and color the points based on their cluster from part (a). Does the PC1 axis, PC2 axis, neither, or both correspond to the clustering?

- Question 1c. Create a heatmap of the expression matrix. Order the genes by cluster, but keep the time points in numerical order.

- Question 1d. Visualize the expression data using t-SNE.

- Question 1e. Using the same data, visualize the expression data using UMAP.

- Question 1f. In a few sentences, compare and contrast the (1) heatmap, (2) PCA, (3) t-SNE, and (4) UMAP results. Be sure to comment on understandability, relative positioning of clusters, runtime, and any other significant factors that you see.

#### Question 2. Sampling Simulation [10 pts]

A typical human cell has ~250,000 transcripts, and a typical bulk RNA-seq experiment may involve millions of cells. Consequently in an RNAseq experiment, you may start with trillions of RNA molecules, although your sequencer will only give a few million to billions of reads. Therefore your RNAseq experiment will be a small sampling of the full composition. We hope the sequences will be a representative sample of the total population, but if your sample is very unlucky or biased it may not represent the true distribution. We will explore this concept by sampling a small subset of transcripts (500 to 50000) out of a much larger set (100k) so that you can evaluate this bias.

In [data1.txt](data1.txt) with 100,000 lines we provide an abstraction of RNA-seq data where normalization has been performed and the number of times a gene name occurs corresponds to the number of transcripts in the sample.

- Question 2a. Randomly sample 500 rows. Do this simulation 10 times and record the relative abundance of each of the 15 genes. Make a scatterplot of the mean vs. variance of each gene (x-axis=mean of gene_i, y-axis=variance of gene_i)

- Question 2b. Do the same sampling experiment but sample 5000 rows each time. Again plot the mean vs. variance.

- Question 2c. Do the same sampling experiment but sample 50000 rows each time. Again plot the mean vs. variance.

- Question 2d. Is the variance greater in (a), (b), or (c)? What is the relationship between mean abundance and variance? Why? How does the mean computed in each subsample compare to the true distribution in the full file?

#### Question 3. Differential Expression [20 pts]

[This file](https://schatz-lab.org/teaching/exercises/rnaseq/rnaseq.2.pileup/rnaseq.2.pileup.tgz) contains a reference genome (`ecoli.fa`), a list of 100 genes of interest (`refgenes.ptt`), and paired-end RNA-seq reads collected from timepoint X for 1 <= X <= 10 (`tX.1.fq`, `tX.2.fq`). The reads are 50bp long from 200bp fragments with errors at a constant 2% error rate.

- Question 3a. Implement [STAR](https://github.com/alexdobin/STAR) in a Docker image. Use [this Docker file](https://raw.githubusercontent.com/slzarate/bwa-mem2-docker/master/Dockerfile) as guidance. Note that STAR is available on [Conda](https://anaconda.org/bioconda/star). You will have to both build the Docker image and push it to [DockerHub](https://hub.docker.com/) (you will have to make a DockerHub account in order to do this). For more information on Docker, see [the documentation](https://docs.docker.com/engine/reference/commandline/cli/). Submit a link to your Docker image on DockerHub.

- Question 3b. For each time point, align the reads to the genome using a WDL constructed around your Docker image. To run the WDL ten times, you can use a bash for loop. For more information about aligning using STAR, see [the documentation](https://raw.githubusercontent.com/alexdobin/STAR/master/doc/STARmanual.pdf). For this question, submit your WDL code.

- Question 3c. After alignment, and for each timepoint, use `samtools depth` to report coverage at each position. Using your own code, report coverage at each position and compute the average depth of each exon.

- Question 3d. Using your own code, merge the depths into an expression matrix (as seen in Question 1). Again, construct a heatmap of the expression matrix over the course of the time series. Identify and list any genes that seem special or otherwise stand out.

### Packaging

The solutions to the above questions should be submitted as a single PDF document that includes all relevant figures (as needed). Make sure to clearly label each of the subproblems and give the exact commands and/or code snippets you used for solving the question. You do not need to show code for plotting. Submit your solutions by uploading the PDF to [GradeScope](https://www.gradescope.com/courses/301857), and remember to select where in your submission each question/subquestion is.

If you submit after this time, you will start to use up your late days. Remember, you are only allowed 96 hours (4 days) for the entire semester!
