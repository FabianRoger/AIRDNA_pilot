

**README**

This Repository contains the code to reproduce the analysis presented in **Airborne environmental DNA metabarcoding for the monitoring of terrestrial insects - a proof of concept from the field** authored by Fabian Roger,  Hamid Reza Ghanavi, Natalie Danielsson, Niklas Wahlberg, Jakob Löndahl, Lars B. Pettersson, Georg K.S. Andersson, Niklas Boke Olén and Yann Clough

There are four RMD scripts are in the folder Scripts/

**16S_Seq_analysis.Rmd** 

this file takes the raw sequencing data demultiplexed for the 16S marker gene and does the sequencing analysis with DADA2. It relies on the external software packages [cutadapt](https://cutadapt.readthedocs.io/en/stable/) and [vsearch](https://github.com/torognes/vsearch) for primer removal, clustering and taxonomic assignment.

this script produces the following files: 

+ 16S_99_Sintax_prob.txt  
+ 16S_99_Sintax_tax.txt  
+ 16S_ASV_table_99.text 
+ 16S_centroids_99.fasta

**COI_Seq_analysis.Rmd**

this file takes the raw sequencing data demultiplexed for the COI marker gene and does the sequencing analysis with DADA2.

+ COI_99_Sintax_prob.txt  
+ COI_99_Sintax_tax.txt  
+ COI_ASV_table_99.text 
+ COI_clustered_99.fasta  

*input*

The demultiplexed raw sequencing files (by sample and primerpair) have been deposited in NCBI’s SRA database under the bioproject number PRJNA757945.

*output*

The files needed for the data analysis are deposited at https://figshare.com/articles/dataset/Airborne_environmental_DNA_metabarcoding_for_the_monitoring_of_terrestrial_insects/16437855

**Data_analysis.Rmd**

This file cleans the OTU tables for both markers, verifies the taxonomic assignment (via Blast) and produces all results presented in the article.

besides the files created by the previous scripts it needs the following metadata files presented on figshare:

+ Insects.txt  
+ Moths.txt
+ Air_DNA_meta.txt  

**Embl_16S.Rmd**

This file documents the process of creating the custom reference database for the taxonomic assignment of the 16S data. It produces the following reference database that we also share on figshare:

+ 16S_SINTAX.fasta

The script relies on the external software [OBITools3](https://git.metabarcoding.org/obitools/obitools3/wikis/home)

 
 

  

