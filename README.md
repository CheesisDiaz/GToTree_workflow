# GToTree_workflow
This is a workflow pipeline for analyzing _Synechococcus_ genomes and creating a Phylogenetic Tree using the guide given by astrobiomike

## How To Create Environment
#### Needed Dependencies 
- GToTree

If you would like to use the envionment used to run this analysis I have already supplied it on the .yml file. All you have to do is to run the code below within this repository:
```
conda env create -f gtotree_env.yml
```
#### Needed Data to Run GToTree
- Genomes to be worked on
- Target genes to be used for the pylogenetic tree (Reference)

## Obtaining Genomes
For this example we used _Synechococcus_ that was already given by the site. 
```
curl -L -o syn-gtotree-example.tar.gz https://ndownloader.figshare.com/files/23629763
```
Were the commands did the following actions:
- curl ; Transfer data from a server
- L ; Define the site from were we'll obtain the data
- o ; Define where we want to store the file or to name is at we require

So based on the command we are downloading the dataset and renaming it syn-gtotree-example.tar.gz to be a compressed archive

To extract the files from the compressed archive we'll use the tar command 
```
tar -xvzf syn-gototree-example.tar.gz
```
Were the commands did the following actions:
- x ; extract the files from the archive
- v ; show the progress of the extraction
- z ; filter the files through gzip
- f ; create files with given filenames

This will create a folder with the following files
- Sequence Genomes Files (fasta files)
- NCBI Assembly accessions (ref-syn-accs.txt)

To input the data we need to list them in a txt file
```
ls *.fa > our-genome-fasta-files.txt
```
Were the commands did the following actions:
- ls ; create a list 
- *.fa ; this will include every file that has a name terminating with fasta type file

## Obtaining Target Genes


## Phylogenetic Tree for Synechococcus Genomes
!["Phylogenetic Tree"](./TreeScaleGenome.PNG)
