2015 hsp evolution extra analyses

###Using hmm scan to identify the number of genes in a particular gene family

#website
http://www.ebi.ac.uk/Tools/hmmer/
#userguide
ftp://selab.janelia.org/pub/software/hmmer3/3.1b2/Userguide.pdf

#workflow
**take nucleotide sequence and search the whole genome

1) My file format is a fasta file, so I need to conver it to stockholm file
using this webpage:
http://sequenceconversion.bugaco.com/converter/biology/sequences/fasta_to_stockholm.php

2) Use hmmbuild to create hmm object from stockholm file
syntax is: hmmbuild <output file name> <input file in stockholm format>
"hmmbuild hsc70.hmm hsc70.stockholm"

3) Do hmmsearch (use nohup nice -n 19 and end with & to run in background)
syntax hmmsearch <input file> <database in fasta format> > <output file>
"nohup nice -n 19 hmmsearch hsc70.hmm Genomes/Aech_2.0_scaffolds.fa > hmmsearch_hsc70_Aech.out &"

it worked!!!
#####RESULTS#############################
Query:       hsc70  [M=1940]
Scores for complete sequences (score includes all domains):
   --- full sequence ---   --- best 1 domain ---    -#dom-
    E-value  score  bias    E-value  score  bias    exp  N  Sequence                 Description
    ------- ------ -----    ------- ------ -----   ---- --  --------                 -----------
          0 2933.7  49.8          0 1871.3   0.2    8.7  8  gnl|Aech_2.0|scaffold121 
     1e-115  388.0   8.5      7e-80  269.2   5.4    3.3  3  gnl|Aech_2.0|scaffold609 
#####END RESULTS#############################

##creating leaf cutter ant database( 2 genomes) to see if I can make 1 big database
1) merging 2 leaf cutter ant genomes
cat Acep_1.0_scaffolds.fa Aech_2.0_scaffolds.fa > leafcutter_genomes.fa

2)hmm search against leaf cutter ant genomes
"nohup nice -n 19 hmmsearch hsc70.hmm Genomes/leafcutter_genomes.fa > hmmsearch_hc70_leafcutter.out &"


####creating full database to hmm scan against#########
#downloaded genomes from antgenomes.org and ncbi
1) merging all genomes and checking if it worked
cat *.fa > insect_genome17.fa
wc -l insect_genome17.fa 
72330091 insect_genome17.fa
wc -l Acep_1.0_scaffolds.fa 
5298782 Acep_1.0_scaffolds.fa

2) hmm searching hsc70-4 against 17 insect genomes
nohup nice -n 19 hmmsearch hsc70.hmm Genomes/insect_genome17.fa > hmmsearch_hsc70-4_17insect_genomes.out &


****17 insect genomes don't work***
separate out by ants, bees/wasp, outgroup

1)constructing ant database
cat Pbar_1.0_scaffolds.fa Sinv_1.0_scaffolds.fa Lhum_1.0_scaffolds.fa Acep_1.0_scaffolds.fa Aech_2.0_scaffolds.fa Cflo_3.3_scaffolds.fa Hsal_3.3_scaffolds.fa > ant_7_genomes.fa

2) bees/wasp database
cat BIMP_2.0_genomic.fa Amel_4.5_scaffolds.fa Bter_1.0_genomic.fa Aflo_1.0_genomic.fa Nvit_1.0.fa > bees_wasp_5genomes.fa

3) outgroup database
cat Dmel_GCF_000001215.4_Release_6_plus_ISO1_MT_genomic.fa Tcas_3.0_genomic.fa B_mori_ASM15162v1_genomic.fa CulPip1.0_genomic.fa Acyr_2.0_genomic.fa > outgroup_4genomes.fa


#*#*#*#*#*#*#*Now we have to do hmm searches for all gene#*#*#*#**#*#*#
gene list:
hsc70-4 
hsc70-3 
hsc70-5

gp93
trap1
hsp83

tccp1
hsp60

hsp40

l2efl


#*#*#*#*#**#*#*#*#*#
gene: Hsc70-4

