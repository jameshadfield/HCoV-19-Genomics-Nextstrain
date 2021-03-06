---
title: "Genomic Analysis of hCoV-19 in San Diego"
authors: "SEARCH-Alliance"
authorLinks: "https://searchcovid.info/"
affilitations: "Scripps Research, Rady Children's Insitute, UC San Diego"
date: "June 2020"
dataset: "https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego"
abstract: "In order to slow the spread of COVID-19 in our community, the SEARCH Alliance is sequencing virus samples from healthcare workers and utilizing publicly available genomic data to track the spread and evolution of hCoV-19."
---

# [Summary](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego?c=region&d=tree&legend=open&onlyPanels&p=full&sidebar=closed)

We analyzed 3383 publicly available hCoV-19 genomes from around the world. 149 of the sequences were sequenced by the SEARCH Alliance from samples collected from individuals in San Diego county between March 11th and May 17th. In this report, we highlight the sequencing results and a few conclusions drawn from a maximum likelihood based phylogenetic analysis  


Table of Contents:  
1. [Data Generation](https://nextstrain.org/community/narratives/andersen-lab/HCoV-19-Genomics-Nextstrain?n=2).
2. [Preliminary Analysis](https://nextstrain.org/community/narratives/andersen-lab/HCoV-19-Genomics-Nextstrain?n=3).
2. [Estimating number of introductions](https://nextstrain.org/community/narratives/andersen-lab/HCoV-19-Genomics-Nextstrain?n=4).
3. [Estimating source of introductions](https://nextstrain.org/community/narratives/andersen-lab/HCoV-19-Genomics-Nextstrain?n=6).
4. [Estimating timing of introductions](https://nextstrain.org/community/narratives/andersen-lab/HCoV-19-Genomics-Nextstrain?n=7).
5. [Scientific Credit](https://nextstrain.org/community/narratives/andersen-lab/HCoV-19-Genomics-Nextstrain?n=8).

# [Data Generation](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego?c=region&d=tree&f_location=San%20Diego&legend=open&onlyPanels&p=full&sidebar=closed)
The 149 sequences from San Diego and the rest of the sequences prepared by the SEARCH Alliance, highlighted to the right, were generated using an amplicon-based sequencing scheme using [PrimalSeq](https://www.nature.com/articles/nprot.2017.066) with [artic nCoV-2019 scheme](https://github.com/artic-network/artic-ncov2019/tree/master/primer_schemes/nCoV-2019).  


Nanopore data was processed using the [artic-nCoV019 pipeline](https://github.com/artic-network/artic-ncov2019) with [minimap2](https://github.com/lh3/minimap2) and [medaka](https://github.com/nanoporetech/medaka).  


Illumina data was processed using [iVar](https://github.com/andersen-lab/ivar) ([Grubaguh et al. Genome Biology 2019](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-018-1618-7)) with [bwa](https://github.com/lh3/bwa).  


All consensus sequences will be deposited on GISAID and on NCBI under BioProject ID [PRJNA612578](https://www.ncbi.nlm.nih.gov/bioproject/612578). Raw read files for both Illumina and Oxford Nanopore data are available on:  

* [Google Cloud](https://console.cloud.google.com/storage/browser/andersen-lab_hcov-19-genomics).  
* SRA under BioProject ID: [PRJNA612578](https://www.ncbi.nlm.nih.gov/bioproject/612578).  

# [Preliminary Analysis](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego?c=region&d=tree&f_location=San%20Diego&legend=open&onlyPanels&p=full&sidebar=closed)
The pipeline used to generate this build is based on the [ncov pipeline](https://github.com/nextstrain/ncov) developed by the Bedford lab.  

Briefly, sequences and metadata were collected from both our repository and [GISAID](https://gisaid.org/). Genomes which were short, incomplete, too divergent, and/or had incomplete metadata were removed from the dataset. We aligned the remaining genomes to reference genome MN908947, and masked problematic sites, based on the following [post](https://virological.org/t/issues-with-sars-cov-2-sequencing-data/473), from the alignment. The alignment was then subsampled to provide context for the San Diego county samples and to reduce computational burden of the analysis. We then generated a phylogentic tree from the alignment using [IQ-TREE](http://www.iqtree.org/) and a time-resolved phylogeny using [treetime](https://github.com/neherlab/treetime). Certain geographic traits, and nucleotide changes were then reconstructed using [Augur](https://github.com/nextstrain/augur).  


# [Estimating number of introductions](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego?c=focal&d=tree&f_location=San%20Diego&p=full&sidebar=closed&legend=closed)
To estimate the number of introductions we infered whether the value of a two-state character (San Diego vs. non-San Diego) for each node in the phylogenetic tree. We then count the number of times a transmission changes from non-San Diego to San Diego. Polytomies containing both San Diego and non-San Diego genomes were conservatively set as non-San Diego and any San Diego genomes which fell on the node were labeled as independent introductions. Looking broadly at the tree, San Diego colored as blue and everything else colored as orange, we can see the San Diego epidemic comprises a very larger number of introductions spread across the tree.  


# [Estimating number of introductions](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego?c=focal&d=tree&f_location=San%20Diego&label=clade:Z1&legend=closed&m=div&onlyPanels&p=full&sidebar=closed)
If we zoom in on one of the larger clades we can see just how numerous the introductions are. Within this clade we can conservativel estimate that there are at least 40 separate introductions. Many of these introductions are likely singletons; we have no evidence they persistent and cause transmission chains. This is consistent with what we know about HCoV-19; we see that only a small proportion of these introductions progress to large transmission lineages. However, an alternative and equally likely explaination is that we have just failed to adequate sample these transmission chains again. We are at the moment sequencing more samples from San Diego to investigate this further.  


# [Estimating source of introductions](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego?c=region&d=tree&p=full&sidebar=closed&legend=closed&onlyPanels&label=clade:Z2)
We can also estimate where these introductions came from. Due to the lack of diversity in the tree, this is difficult to determine for a lot of introductions. However, we can estimate the introduction source based on where similar sequences were found before we sampled them in San Diego. For the clade on the right and in a majority of introductions across the entire tree, Europe is the source. This is despite the fact that national travel far outweights international travel into San Diego.  


However, it is fair to say that both internation and national importation play a role in the epidemic in San Diego as we also see introductions from elsewhere in the United States, particularly other California and West Coast locations. It is also important to consider that this tree is quite undersampled, especiallyin the United States. Lack of samples from other states hinders our ability to determine the source of HCoV-19 introductions into San Diego definitively as we might have not yet sampled the intermediate sequences.


# [Estimating timing of introductions](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego)
Lastly, we can further estimate with this time-resolved phylogeny that the vast majority of introductions occured between February and Early March. The plot on the right shows the number of estimated introductions that have occured in San Diego per day since the begining of the pandemic. The date of introduction is estimated as the time of the most recent common ancestor of each detected San Diego transmission lineage.  


On the graph, we can see that introductions start to occur around mid January and have continued consistently into late April, which is when the lattest sequences were sampled. We can also see that while introductions have not stopped, they do seem to have peaked in late March, coinciding with the state-wide stay-at-home order by Governor Newsom on March 19th, and the barring of entry to foreigh nationals on March 20th.  


```auspiceMainDisplayMarkdown
<img src="https://raw.githubusercontent.com/andersen-lab/HCoV-19-Genomics-Nextstrain/master/img/introductions_filterd.png" alt="Introductions into San Diego">
```


# [Scientific Credit](https://nextstrain.org/community/andersen-lab/HCoV-19-Genomics-Nextstrain/hCoV-19/usa/sandiego?c=region&d=map&label=clade:Z1&legend=closed&onlyPanels&p=full&sidebar=closed)
**Disclaimer**. Please note that this data is still based on work in progress and should be considered preliminary. If you intend to include any of these data in publications, please let us know – otherwise please feel free to download and use without restrictions. We have shared this data with the hope that people will download and use it, as well as scrutinize it so we can improve our methods and analyses. Please contact us if you have any questions or comments – we’ll buy beers for #ResearchParasites that spot flaws and faults in the data and come up with improvements!

---
**Andersen Lab**  
The Scripps Research Institute  
La Jolla, CA, USA  
[data@andersen-lab.com](mailto:data@andersen-lab.com).


