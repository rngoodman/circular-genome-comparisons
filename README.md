# Circular Genome Comparisons

![Example Plot](figures/9A-2-7_vs_9A-1-1_no_text.png)

## Quick start

Here is my [code for visualising genome comparisons in a circos plot](https://rngoodman.github.io/circular-genome-comparisons/circular_genome_comparisons.html) between two genomes compared with [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi). 

## About 

This workflow uses [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) for sequence alignment, parses the results, and visualises the differences using [circlize](https://doi.org/10.1093/bioinformatics/btu393) in R (based on the original [circos](https://circos.ca/) plot).

I wanted to visualise the comparison of all contigs of my genomes within one figure and a circular visualisation seemed the best way to do this.

Using circos plots to visualise genomic comparisons is useful for several cases such as:

* Mobile Genetic Element (MGE) transfer
* Evolutionary studies comparing ancestor strains with progeny strains
* Comparison of newly sequenced strains to reference strains

## Considerations/limitations

* You can define the percentage identity and length of the comparative site in bp. 

* This workflow uses BLAST to align the genomes but other comparison tools could be used e.g. mummer. The parsing of the file into R would just need tweaking and checking that table headings match up.

* You need to have [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi) and [seqkit](https://bioinf.shenwei.me/seqkit/) downloaded and in your path for the initial steps in bash. I have included the outputs of these steps under the data folder of this repository so that you can load them directly into R if necessary. 

* It works better for long-read/hybrid assemblies with < 10 contigs than short-read assemblies with > 50 contigs. 



