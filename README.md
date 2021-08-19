# Notebook and protocols
### Author: Andrew D. Nguyen    
### website: https://adnguyen.github.io/    
### email: anbe642@gmail.com   
Date started: 2016-10-04    
Last date modified: 2021-08-19    

This repo shares my protocols and notebooks of ongoing work with the aim of capturing the process of science as it is happening and making it transparent and reproducible. Template for making an online notebook found [here](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/Online_notebook_template.md). View github repo [here](https://github.com/adnguyen/Notebooks_and_Protocols).

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
------



# List of Notebooks by year    

* [2019_Notebook](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2019_notebook.md)     

  * dissertation (ants) and post doc projects (Rhagoletis)
  * cerasi dataset brain transcriptome analysis 

* [2018_Notebook](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2018_notebook.md). This notebook log:
  * dissertation projects (hsp rxn norm, range limits, proteome stability project, stressed in nature, thermal niche)
  * post doc projects (biological rhythms of *Rhagoletis*, meta-analysis of biological rhythms)
  * paper readings on biological rhythms and thermal adaptation
* [2017 Ecoological Genomics Notebook](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2017_Eco_Gen_ANBE_nb.md). This notebook logs the activities throughout the semester    
  * I was a TA for Pbio381 at the University of Vermont, Spring 2017   
  * Check out our overall [workflow](Images/Overall_workflow_eco_genomics.html)
  * We learned:
    * different sequencing platforms and strategies
    * population genomics- Admixture, demography
    * differential gene expression with RNA-seq
    * gene annotation with BLAST and GO    
* [2017_Notebook](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2017_notebook.md): This notebook logs     
  * climate cascade meetings and projects (dissertation work)
  * Conferences (SICB)
  * Writing notes for dissertation
  * Paper readings on Hsps; proteasome, tolerance vs resistance
* [2016_Notebook](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2016_notebook.md): This notebook logs:
  * climate cascade meetings
  * related climate cascade projects (Hsp modulation paper; thermal niche paper; Adaptive shifts in Hsp gxp as a function-valued trait paper; proteome stability project; range limits paper
  * post doc ideas (selection gradients, quantitative genetics in natural populations)
  * journal clubbing by myself- indirect genetic effects, Kingsolver phys model, membrane stability
  * fixing machines - ABI steponeplus
  * curve fitting for subsets of dataset
  * Evolution meeting
  * Phylogenetics of Aphaenogaster    
* 2015 (before I found markdown, so these aren't perfectly formatted)    
  * [HMM scans](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2015_hmmscan_notebook.md)
  * [RAD-seq phylogenetics](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2015_phylogenomics_rad_seq_ANBE.md)   


# List of protocols   

### University of Vermont lab protocols  

* [Heat shocking, RNA isolations, and QPCR](https://github.com/adnguyen/Notebooks_and_Protocols/blob/master/2016_ANBE_protocols.md)
* [Protein related](https://github.com/adnguyen/2016_Protein_stability_evolution/blob/master/Documents/Protocols/Protocols.md)

###[University of Florida, Hahn Lab protocols](https://adnguyen.github.io/Hahn_lab_protocols/)

# Notes

Referencing some syntax for pandoc for converting md to html:

```
pandoc -o output.html input.txt
```   

Cool snippet of code for dempster-shafer combination using yager method: 

```R
#data set
dd<-data.frame(rbind(c(0.5,.25,.25),c(.25,.5,.25),c(.2,.6,.2)))
##write the function 
dst.fun<-function(data=dd){
  y<-vector("list",nrow(data)) # create a list with length of the rows of data
  
  #for loop to create a mass function for each row of data
  for(i in 1:nrow(data)){
  row<-data[i,]
  state<-c("a","b") #specify state space
  weight<-mass(list("a"=row[,1],"b"=row[,2],"a/b"=row[,3]),state) # assign mass to state spaces
  y[[i]]<-weight
  }
  
  
  mm<-setNames(y,paste0("mass",1:nrow(data))) # populate the list with masses
  dat<-data.frame(focal(EvCombR::yComb(mm))) # grab the mass values from combining all sources of evidence 
  names(dat)<-c("positive","negative","both") # rename 
  return(dat)


}

dst.fun()

```


