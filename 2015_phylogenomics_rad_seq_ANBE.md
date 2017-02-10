##2015
##Andrew Nguyen 
##Raxml notebook


------------------------
20150819
------------------------
**I need to run 2 trees through raxml and 1 through beast

#I'm running raxml from the executables in the file
#i could put it in the 'bin' but It doesnt' work


##General command for constructing a phylogeny
#-s file specifies input
#-n is the output
#-m is the model 
./raxmlHPC -f a -s ~/Desktop/20150818_Andrew_SNP_sequences_nooutgr.fasta -n 20150819_commongarden_raxml_v2 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345

#Now that I have the command, I want to rund stuff in the background
http://johnstantongeddes.org/computing/2013/05/07/workstation-guidelines.html
---following JSG's guidelines, here is the code:
"nohup nice -n 19 Rscript script.r &"


#ok, lets see if this works:
###command for my common garden experiment without outgroups
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/20150818_Andrew_SNP_sequences_nooutgr.fasta -n 20150819_commongarden_raxml_v2 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &


##ok, let's run a raxml phylogeny for the JSG_phytotron dataset
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_JSG_phytotron_trees/20150817_JSG_phytotron_SNP_sequences.fas -n 20150819_JSG_phytotron_v2 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

------------------------
20150824
------------------------
Raxml can actually calculate a pairwise ML distance matrix

example: "raxmlHPC -­f x -­p 12345 -­s alg -­m GTRGAMMA ­-n TEST"

###JSG phytotron tree
command used:
nohup nice -n 19 ./raxmlHPC -f x -p 12345 -s ~/Desktop/2015_JSG_phytotron_trees/20150817_JSG_phytotron_SNP_sequences.fas -m GTRGAMMA -n 20150824_JSG_phytotron_pariwise_ML_distancnoe -t ~/Desktop/2015_JSG_phytotron_trees/RAxML_bestTree.20150819_JSG_phytotron_v2 &

##ANBE common garden tree

##for anbe tree, claculate pairwise ml distance matrix
nohup nice -n 19 ./raxmlHPC -f x -p 12345 -s ~/Desktop/2015_ANBE_common_garden/20150818_Andrew_SNP_sequences_nooutgr.fasta -m GTRGAMMA -t ~/Desktop/2015_ANBE_common_garden/RAxML_bestTree.20150819_commongarden_raxml_v2 -n 20150828_commongarden_pairwise_ML_distance &

------------------------
20150924
------------------------
trying out raxml under 2 sets of stringencys (M1 and M2)

##for m1 no outgroup other than v messor
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Stringency_m1_m2/Andrew_SNP_sequences_m1_Aph_Vmessor.fas -n 20150924_m1_stringency_anbesamples_nooutgroup -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &


###for m5 no outgropu other than v messor

nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Stringency_m1_m2/Andrew_SNP_sequences_m5_Aph_Vmessor.fas -n 20150924_m5_stringency_anbesamples_nooutgroup -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &


------------------------
20151026
------------------------
###for m3 no outgropu other than v messor

nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/20151026_M3_anbe_SNP_v2.fas -n 20151026_m3_stringency_ANBE -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

------------------------
20151102
------------------------
reconstructing 3 trees

***m1_3SNP***
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/SNP_sequences_m1_3SNPs.fas -n 20151102_m1_3SNP_anbe_common_garden -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

***m3_6SNP***
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/SNP_sequences_m3_6SNPs.fas -n 20151102_m3_6SNP_anbe_common_garden -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

***m5_3SNP***
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/SNP_sequences_m5_3SNPs.fas -n 20151102_m5_3SNP_anbe_common_garden -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

------------------------
20151120
------------------------
##using Novomessor as outgroup using phytotron catalog or ANBE catalogs

#new catalogs

#m1
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Nmessor_outgroup/20151120_new_cat_nov_m1.fas -n 20151120_new_cat_Nov_m1 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &
#m3
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Nmessor_outgroup/20151120_new_cat_nov_m3.fas -n 20151120_new_cat_Nov_m3 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &
#m5
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Nmessor_outgroup/20151120_new_cat_nov_m5.fas -n 20151120_new_cat_Nov_m5 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

# phytotron catalogs
#m1
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Nmessor_outgroup/20151120_Nmes_m1.fas -n 20151120_phytocat_Nov_m1 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

#m3
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Nmessor_outgroup/20151120_Nmes_m3.fas -n 20151120_phytocat_Nov_m3 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &

#m5
nohup nice -n 19 ./raxmlHPC -f a -s ~/Desktop/2015_ANBE_common_garden/Nmessor_outgroup/20151120_Nmes_m5.fas -n 20151120_phytocat_Nov_m5 -e .1 -m GTRGAMMA -x 12345 -#100 -p 12345 &









