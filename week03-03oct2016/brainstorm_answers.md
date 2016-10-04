
# Part 1 - Brainstorm: Statistics

## Distributions
### e.g., Gaussian, Poisson, ..

## Statistical Models
## Methods for Estimation
## Methods for Hypothesis Testing

# Part 2 - Brainstorm: Technologies in Biology

## microarray, sequencing, etc.

## In-class exercise 1 (1 technology for each row): microarray, Illumina seq, other types of seq

### Goal: 
#### produce a 2-3 point summary
#### links to a few (<5) good resources
#### add your description to the #technology_day slack channel (add all github usernames of your group!)

# Part 3 - Brainstorm: Applications in genomics 

### e.g., gene expression

# Part 4 - Brainstorm: Linking Technologies to Applications to Statistics (mainstream)

## e.g., microarray -> gene expression -> normally distributed (log intensities)

## In-class exercise 2 (in groups/rows): 
### Goal: make the link between technologies, what is measured, statistical models used
### For example:
##### RNA-seq: sequencing -> gene expression -> ?
##### BS-seq: bisulphite + sequencing -> DNA methylation -> ?
##### ChIP-seq: sequencing -> protein/DNA interactions -> ?


# Part 5 - Brainstorm: Methods/algorithms/data structures that are associated more to computer science

# Part 6 - Pick another "technology" (from those above or from [1]) to briefly describe

## In-class exercise 3 (in groups): 
### Goal: 
#### write ~2 sentences about what the method does
#### again, make the link (technology -> application -> statistics)
#### list the github usernames of everyone in your group
#### submit a pull request to brainstorm_answers.md

##### CNV-seq

_(payne76, ellereve, pbieberstein, abhimanyusahai, duoa, paulacarrio)_

CNV-seq is a shotgun sequencing method used to detect copy number variation (CNV). Shotgun reads from two samples are mapped by sequence alignment on a template genome and analyzed with a sliding window approach so that number of reads per window for each sample can be computed and combined into a ratio. The number of reads in a sliding window is poisson distributed with mean number of reads/window, $\lambda$, depending on total number of sequenced reads N, the size of the sliding window W, and the size of the genome G, where W is much less than G, but when mean number of reads per window is more than 10 with continuity correction, we may use a gaussian approximation for the poisson (Number of reads in sliding window $\sim N(\mu=\lambda, \sigma^{2}=\lambda))$. After a transformation, the ratio between the two samples is $\sim N(0,1)$, when mean number of reads per window in sample y is more than 6 and less than 40,000 in sample x.

[1] [https://liorpachter.wordpress.com/seq/](https://liorpachter.wordpress.com/seq/)


