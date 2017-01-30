# 2017 Ecological Genomics Course

### Author: ANTdrew D. Nguyen     


## Overall Description of notebook      
I am the teaching assistant, but I will follow the tutorials and log what I've done here. 

## Date started: (2017-01-18)   
## Date end:   ongoing    

## Philosophy   
Science should be reproducible and one of the best ways to achieve this is by logging research activities in a notebook. Because science/biology has increasingly become computational, it is easier to document computational projects in an electronic form, which can be shared online through Github.    


<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.  


### Table of contents for 60 entries (Format is *Page: Date(with year-month-day). Title*)        
* [Page 1: 2017-01-18](#id-section1). First class; intros
* [Page 2: 2017-01-20](#id-section2). Readings for 2017-01-23 Monday    
* [Page 3: 2017-01-23](#id-section3). Week 2, Day 2, course notes
* [Page 4: 2017-01-25](#id-section4) . Week 2, Day 3, class notes (paper discussions and student project development)
* [Page 5: 2017-01-30](#id-section5). Week 3, Day 4, class notes , Group presentations of project ideas
* [Page 6:](#id-section6).
* [Page 7:](#id-section7).
* [Page 8:](#id-section8).
* [Page 9:](#id-section9).
* [Page 10:](#id-section10).
* [Page 11:](#id-section11).
* [Page 12:](#id-section12).
* [Page 13:](#id-section13).
* [Page 14:](#id-section14).
* [Page 15:](#id-section15).
* [Page 16:](#id-section16).
* [Page 17:](#id-section17).
* [Page 18:](#id-section18).
* [Page 19:](#id-section19).
* [Page 20:](#id-section20).
* [Page 21:](#id-section21).
* [Page 22:](#id-section22).
* [Page 23:](#id-section23).
* [Page 24:](#id-section24).
* [Page 25:](#id-section25).
* [Page 26:](#id-section26).
* [Page 27:](#id-section27).
* [Page 28:](#id-section28).
* [Page 29:](#id-section29).
* [Page 30:](#id-section30).
* [Page 31:](#id-section31).
* [Page 32:](#id-section32).
* [Page 33:](#id-section33).
* [Page 34:](#id-section34).
* [Page 35:](#id-section35).
* [Page 36:](#id-section36).
* [Page 37:](#id-section37).
* [Page 38:](#id-section38).
* [Page 39:](#id-section39).
* [Page 40:](#id-section40).
* [Page 41:](#id-section41).
* [Page 42:](#id-section42).
* [Page 43:](#id-section43).
* [Page 44:](#id-section44).
* [Page 45:](#id-section45).
* [Page 46:](#id-section46).
* [Page 47:](#id-section47).
* [Page 48:](#id-section48).
* [Page 49:](#id-section49).
* [Page 50:](#id-section50).
* [Page 51:](#id-section51).
* [Page 52:](#id-section52).
* [Page 53:](#id-section53).
* [Page 54:](#id-section54).
* [Page 55:](#id-section55).
* [Page 56:](#id-section56).
* [Page 57:](#id-section57).
* [Page 58:](#id-section58).
* [Page 59:](#id-section59).
* [Page 60:](#id-section60).

------
<div id='id-section1'/>
### Page 1: 2016-07-18. Ecological genomics, first class

### **Steve and Melissa's intro**    
* Steve: It is a young field, trying to establish it's own identity    
  * Ecological genomics institute, KSU: emphasis on adaptation to environment   
  * Gordon Research Conference: Integrating different levels of biological organization on **ANY SYSTEM**; approach and tool focused! Field going towards new data and new analytic techniques  
  * Intro to eco genomics, oxford press; Using technology to address ecological issues such as nutrient cycling, population structure, life history vairation , trophic interaction, stress responess, and adpatation to environmental change   

* DATA driven: next gen sequencing revolutionizes biology
  * creats a new problem--large datasets!!! how to make sense? 
  * not data limited and potentially computationally limited   

* Where is the field headed    
  * Molecular Ecology Journal(flagship journal representative o the field)  
    * ALL systems:  corals, protists, daphnia, coral, lemurs, dandelions, steve studies trees 
    * model organism constraint disappearing!   
  * What types of questions are asked?  
    * How do genes correspond with circadian rythm?  
    * How does the microbiome influence the organism? 
    * How does epigenetic variation influence evolutionary responses? or contribute to phenotypic variation?  
    * What are the patterns of genetic diversity that can give us insights on population dynamics?  
    * What are constraints and tradeoffs and genetic mechanisms of traits? 

* Methods?   
  * De novo genome assembly; sequencing a DNA book from scratch!!    
    * RNA-seq; transcriptomic profiling     
  * 16 s metagenomic sequencing      
  * Rad-seq/GBS for estiamting population structure and genetic diversity     

* Proccesses studied?    
  * All evo and eco stuff; speciation, hybridization, local adaptation, genetic basis of local adaptation, genetic architecture of complex phenotypes, genes controlling host-pathogen evolutionary dynamics, pop structure, gene flow, epigenetics     

* Goals of the course!    
  1. Learn how ecology and genomes shape each other   
  2. Think creatively about major questions, and pose testable hypotheses to those questions using appropriate genomic data    
  3. Think about careful experimental design and statistical analysis---shown by reading papers   
  4. Achive working knowledge and level of comfort for bioinformatics routines for ecological genomics studies   

  ### Melissa background  

**Background, what drove Melissa and Steve to ecological genomics?**       

Melissa read a cool paper that scales from analyzing a few loci to the whole genome.   

One figure popped out at her, FST (developed by Sewell Wright) histogram.   FST of 1= complete differentiation, FST of 0 = no diff. FST described as **Alleles in space**. From this histogram, Melissa was struck by how you can separate out neutral from selective ones.  

Melissa has a data set with 96 sea stars and then the 16s microbiome. Would be cool to see if there is heritability in some bactera

### Steve background   

* Inspired by Yanis Antonivics (an **OG**)   
* At the time, just so stories: **Adaptatationist programme**    
  * Just go out and go by feeling in a natural history way and prescribe an adaptation story   
  * Janis wrote a creed to quantify the operational relationship between traits, environment, and genetics     
* Yanis was on Steve's committee and Steve was interested in adaptation with respect to invasion biology because organisms need to respond to novel environments     
  * Phenotypes can relate to the environment, but what is the genetic basis of local adaptation (in situ)? There are other confounding issues: demographic effects, plasticity     
* Steve thinks about environment-phenotype-genetics triangle. Basically a path diagram that feeds back on each other.    
  * Relationship between genes and phenotype ---GWAS (Genome wide association study)    
  * Relationship between genetics and environment --- Fst, clines between allele frequencies and environment    
* Invasion history is tough because of demographic history    
* He decided to focus on trees; large population size, straddle huge environmental gradients so the opportunity for selection is high   
  * positive relationship between Growing season length and traits    
  * Did a  reciprocal transplant of different populations to identify the extent of local adaptation in large established common gardens    
  * SK does GBS (genotype by sequencing)      
  * Problem with field: validating key gene candidates            


------
<div id='id-section2'/>
### Page 2: 2017-01-20. Readings for 2017-01-25 Monday    

First, showing how I structured the readings in the repo: 

1. In the terminal, change directory into your repo

```
cd Teaching/2017_Ecological_Genomics/
```

For fun, list the items in your repo
```
ls
01_data				Online_notebook.md
02_scripts			README.md
03_results_output		index.Rmd
04_tutorials			index.html
2017_Ecological_Genomics.Rproj	index.pdf
ANBE_notebook.md		papers

```

2. Now use tree command to extract hierarchical layout     

```
tree
.
├── 01_data
├── 02_scripts
│   └── RasterPCA_demo.Rmd
├── 03_results_output
│   └── RasterPCA_demo.html
├── 04_tutorials
├── 2017_Ecological_Genomics.Rproj
├── ANBE_notebook.md
├── Online_notebook.md
├── README.md
├── index.Rmd
├── index.html
├── index.pdf
└── papers
    └── 01_week
        └── 01_Day_Monday_2017-01-25
            ├── Ellegren_2014.pdf
            ├── Lee_gould_stinchcombe_2014_AoB_PLANTS.pdf
            └── Rockman-2012-Evolution.pdf

```

So my plan is to place my papers in the "papers" directory, within a particular week, and then within a particular day number of the course that is annotated with the actual day and date.  

### Now paper notes:    

1. Genome Sequencing and population genomics in non-model organisms ; Hans Ellegren    

   * 3 important achievements in bio over the past century: modern synthesis(evolutionary theory), mol bio, and "omics" era   
     * Good example of how biologists can get carried away with "omics" or "omes"   
     * peptidome, degradome,     
   * Basically,  because we can sequence everything we can collect, we can study non-model organisms like never before.  
   * In fact, many genomes are sequenced   
   * Bird example: Chickens were sequenced first, then zebra finch, then a bunch of others, highlighting the rapid ability to sequence genomes   
   * Genomic information is nice because it can tell you how loci are arranged. Example, recombination can be better studied by knowing the arrangement of chromosomes.   
   * Having genomic sequences allows for us to compare the repertoire of genes and the actual sequences themselves. (birth and death evolutionary procceses in homologues; tests for positive selection)

2. Identifying the genes underlying quantitative traits: a rationale for the QTP programme; Lee et al. 2014
   * QTN = quantitative trait nucleotide; associating single nucleotides with quantitative traits    
   * Critical question: What is the molecular basis for adaptation? particularly in non-model organisms
   * Response to Rockman 2012 paper    
     * Rockman's major criticisms: Effect of nucleotide on traits can be overestimated    
       * large effect variants are rare and most complex traits are polygenic    
   * Travisano and Shaw 2013 raise the criticism that you don't need QTN's to focus on the patterns and process of adaptation    
     * knowing molecular basis has not illuminated the proceess of adaptation!    
   * 5 reasons why we should care about QTNs     
     1. Vertical Integration: nucleotide to ecosystems        
     2. Parallel evolution and pleiotropy     
     3. Maintenance of standing genetic variation    
     4. Role of standing genetic variation in adaptation     
     5. Understanding the role of genomic architecture in adaptation      

------
<div id='id-section3'/>
### Page 3: 2017-01-23. Day 2, course notes      

### Course materials    
-Papers- info updates, and discussion papers; students need to sign up   	


**Add definitions as you see it**    

**Info update rubric**    
* Outline   
* 20 min   
* Learning/engaging activity   
* use board effectively   
* take home messages    
* samples from the literature   

### Glossary:     

*Reads*: a length of sequenced DNA      
	* short = 50 bps; long = 100, 150, 300, 10,000-60,000 bps     
	* could be single or pair-end ( 1 strand or both strands)    


### Melissa info update: 
1. Advances of sequencing technologies    
2. Range of Applications   
3. General workflow (usually involving building libraries to be sequenced )    
4. Sequencing by synthesis (SBS)     
5. Other technologies of SBS    
6. Learning activity    

### 1. Advances of sequencing technologies    

Good example was the human genome project:   

* finished in 2001 or 2003 or so   
* used with sanger sequencing on ABI platform   
* it took **15 years of intense effort** for 1 person's genome at the cost of $3 billion dollars

Then, Illumina released Hi seq X Ten sequencer in 2014   
* **In a single day, they could sequence 45 whole geomes for $,1000 for each!!!**   
* 90% of global data now       

* Good example of how costs went down, but data went up!     

Illumina sequencing:   
Similar to sanger but fluorescence can be observed across a whole "field".   

### 2. Range of Applications     

1. Whole genome sequencing    
2. RNAseq    
3. Chip-seq    
4. Capture-sequencing; design probes and hybridize it with sample (it is targeted)        


### 3. General workflow (usually involving building libraries to be sequenced )    

Step 1: Goal-oriented; which platform to use?   

* where genetic variation is    
  * Phenotypes     
  * number of samples
  * population    
  * individual   
  * comparative study? closely related species?    
  * model organism or not?   
* demographic history?     
* adaptive gentic variation     
* gene expression variation under common garden conditions?   


**Trade-offs in doing the actual sequencing**   
* length of reads     
  * long reads are easier to assemble(piece genomic regions together)       
* # of reads    
  * 10 million per individual?  target capture does not need too many reads    
* how read are distributed along the whole genome      


**Actual workflow now** 

1. Extract DNA or RNA(this needs to be converted into cDNA)   
2. Fragment sample (break it into smaller junks)    
3. Ligate adapters on the ends 
   * Often barcoded to identify samples/individuals      
4. Add on sequencing adaptors      
5. PCR amplification        

### 4. Sequencing by synthesis (SBS)     

1. DNA with different adapters   
2. get loaded into 1 of 8 lanes in a flowcell   
3. flowcell have oligos that match the sequencing adaptors; so DNA attaches to it! (P5 and P7)    
4. Bridge amplification: bend over and amplify, back and forth, over and over    
   * creates a clustered generation; sequence of the exact same sequence locally as a dot    
5. Incorporates labeled A T G or C, and then images are taken across the whole flowcell  

**Pac-bio's platform: Single molecule real time sequencing (SMRT)**     
1. DNA frag in a well, light penetrates in a small area to capture sequencing with long reads    

### 6. Learning activity    

1. pair with neighbor   
2. share ah-ha moments   
3. discuss some useful applications    


### Paper discussions  : Genome sequencing and population genomics in non-model organisms (Hans Ellegren )    

* Why would we use it ?    
* SK- we're generating tons of data, but what is the limit of space we can store it in ? (Short read archive)      
* NCBI, who curates the data? Wild west.      
* 10-15 gbs for 1 file of in gzip format    
* Table 1; 2200 eukaryote genomes vs 600 listed in this paper     
* How do people choose which genome to sequence? politics   
* Can people ID species based on WGS?   
* Are there multiple references genomes assembled?    
* From a single individual, do people overlay as many omics as possible? Integrate proteome, PTMs, metabolome, phenotypes, etc    

### The future! Moving forward    
* 1 week from today, do a blitz on the different library preps (4 different ones)      
  * 4 diff info updates    
* 2 volunteers to discuss QTN programme.    
* Each student, 1 discussion leader and 1 info update!   


 

------
<div id='id-section4'/>
### Page 4: 2017-01-25. Week 2, Day 3, class notes (paper discussions and student project development)

**Tasks**

One of my duties is to populate the glossary on blackboard. (I'll do it here for redundancy too.)



**Restructured course layout**: 

```
.
├── 01_data
├── 02_scripts
│   └── RasterPCA_demo.Rmd
├── 03_results_output
│   └── RasterPCA_demo.html
├── 04_tutorials
├── 2017_Ecological_Genomics.Rproj
├── ANBE_notebook.md
├── Online_notebook.md
├── README.md
├── index.Rmd
├── index.html
├── index.pdf
└── papers
    └── 01_week
        ├── Ellegren_2014.pdf
        ├── Lee_gould_stinchcombe_2014_AoB_PLANTS.pdf
        └── Rockman-2012-Evolution.pdf
 6 directories, 12 files
```

It better reflects how the reading is done throughout the week.    

### Course outline

1. Announcements: 
   * BB acceess: add through audit
   * Sign-ups   
   * Glossary: Whoever is doing info update must come up with a list of key terms!      
2. Info update ~ QTN   
3. Debate-style discussion 
4. BREAK   
5. Group project discussion!   

### 1. Info update ~ QTN 

**Q: What are QTN's (Quantitative Trait Nucleotide)?**   

* **Quantitative genetic theory of adaptive traits**   
  * Additive genetic variance and heritability 

QTN is the most reductionist you can get. The individual SNPs that contribute to the variation in a trait. Usually traits under selection and confer adaptation.  

Traits!

	1. flowering time
	2. flower color
	3. thermal tolerance 
	4. venom potency
	5. defense or secondary compounds in plants  
	6. toxin tolerance  
	7. drought tolerance 
	8. altitude tolerance (hypoxia)

They are quantitative, and are continuous. They have a mean and variance. **Not descrete phenotypes**. Discrete phenotypes are mendelian (major effect loci) .   

Modern synthesis (Fischer, Haldane, WRight).  Connect alleles with trait distribution. 

ex:  allele:trait

AA = 1

Aa = 2

aa = 3

The difference between Aa and aa = average effects or alpha (1).

AA = q^2 

Aa = 2pq

aa= p^2 

Additive genetic variance (Va) = sum of alpha * pi and qi.   pi and qi 

Vp = phenotypic variance and the Va is only a fraction. So the heritability is Va/Vp.  



**What are the genes that explain this heritability? Alpha is the effect size of the QTN**

Most populations are close to their adaptive peak. Imagine fitness as a fucntion of a trait, normal distribution.  Max fitness = intermediate trait is local adaptation. Change in environment will change the fitness peak. 

A mutation is random, and it can move the fitness of the population up or down. This is usally a small effect mutation. But if you have a large effect mutation, then changes are, you will move down, maintain, or up, but if it pushes too far, it'll go down. It is must more effecient for the population to evolve many small effect loci.  How do we detect this?

**3 main methods**

1. **QTL mapping (forward genetics)**
   * Segregating sites between 2 individuals (red vs blue) and they're diploid
   * They're homozygous (2 extremes of trait)
   * Take parents, cross to make F1—that are heterozygous
   * Take F1s, and do a series of cross to produce F2
   * The chromosomes that vary in the ancestry of different blocks(chromosome)
   * The QTL or QTN is unknown (trait based forward genetics approach)
   * Markers (microsats) and unlinks them (because of the crossing) 
   * By multiple rounds of generations, then you get variation in loci size
2. **GWAS (Genome-wide association studies) (forward genetics)**
   * Let nature do the crosses, and sample a bunch of individuals
   * genotype them, 
   * Nature has been doing a similar experiment as in the QTL mapping but there are many more parents
   * Model: Y = u + Bi x SNPi + Covariates
     * Y = Trait 
     * u = intercept
     * Bi = effect size
     * SNPi= a particular SNP
     * Covariates = population structure 
   * You get a manhattan plot, plotting -log(pvalue) against position
     * High values indicate significant SNPs 
     * usually includes several genes although it will involve many genes
3. **Selection Scans (reverse genetics)**
   * don't know trait, just zoom in on parts of the genome that have history of selection
   * Sample a bunch of individuals, with a bunch of SNPs  
   * Selective sweep, some rise in frequency and others are not  
   * Over T generations, it could fix—DECREASING diversity 
     * iF this varies among populations, then this could indicate selection and divergence (FST)
     * data shows us what genes are important when we did not know *a priori*



Additional notes: Mutations before selection are equal across loci and their effect sizes. So after selection, the frequency of effect sizes are concentrated on the small values(small effect sizes) and very little at the large effect size.  

### 3. Debate-style discussion ("QTN programme")   

2 separate groups discussions first.

**Dr. Brody leading Rockman paper**: 

* analogy: panning for gold, large nuggets already found, and now we're finding needles in a haystack 
* large effect QTLs, very few cases found, but that is not most of them  

3 main arguments

1. LARGE effect QTLs are mendelian 
2. Theory does 
3. searching for QTNs may act in the same way as large effect QTL 

Speciation example: Doug Schemsky

They speciated because they got different pollination syndromes (changed from yellow to red). It acted like a mendelian trait. Is it important in knowning speciation?  Is it common? Speciation can be neutral just by building up different genetic interactions that leads to reproductive isolation. 

**Whole group Discussion**   



### 5. Student Project development 

Melissa's dataset

Seastar wasting disease: kills stuff, **PATHOGEN UNKNOWN** 

* Some species are resistant and some rae susceptible
* it is a generalist 
* A couple days or even hours that a host goes from healthy to sick
* Sickness comes in the form of losing arms, lose turgor pressure, they become droopy
    * start off with legions and/or loss of turgor pressure
    * loss of limbs = gravity and/or behavioral (when they move,t heir body doesn't stay together)
    * turn into a puddle of white goo; ghostly shapes of sea stars ; so sad
* **Potentially Densovius is causal** (maybe)
* What factors affect the tipping point? 
* Sampled epidermal biopsy
    * total RNA isolation, polyA tail selection to get mRNA
    * 300 million paired end bp sequencing
    * took out 16s rRNA 


**Hypotheses** 

Theme: 

1. What is the genetic difference related to susceptibility
   * Int or sub tidal are more susceptible 
   * int or sub differ in gene expression 
2. What is the genetic basis for disease resistance? 
   * positive selection on genes and how they're related to health/symptoms
3. How does the microbiome contribute to seastar wasting? 
   * microbiome differ among disease/symptoms
     * diversity? abundance?
4. Is there heritable genetic variation in the microbiome? 



Course notes for next week:

1. put picture of all of our hypotheses on the screen
2. 4 corners of the room, put interests and groups will assemble
3. give half of class to think through and other half to present ideas 
4. Make students formulate questions, hypotheses, predictions, what samples
5. Technical questions: construct assembly together? separate? Give students a canonical reference (transcriptome). let students investigate if they want to separate them. 
6. Melissa and Melanie will do the assembly on the side.   
7. AN will be added as adminstrator access (permission changes and stuff); software installed, 
   * add trinity
   * AN can install 
8. Wednesday, hands on logging in on the server, Unix command lines  
   * have shell, have putty
   * connect remote machine
   * set up home directory
   * move around in the machine
   * regular expression 
   * moving , cutting, copying files
   * transfer between server and client
9. Look at wiki to see what we can add or subtract in terms how what commands to show  



Set up new webpage for course: 

1. links to tutorials
2. scripts
3. page with class members with hyperlinks to their github notebooks 
4. (**Getting set up link**)New tab with resources for markdown and online notebook and typora
5. Glossary link to blackboard


### Changing the course material to construct a website: 

```
.
├── 04_tutorials
├── 2017_Ecological_Genomics.Rproj
├── ANBE_notebook.html
├── ANBE_notebook.md
├── Class_members.Rmd
├── Class_members.html
├── Getting_started.Rmd
├── Getting_started.html
├── Instructors.Rmd
├── Instructors.html
├── Online_notebook.md
├── PBIO.BIO381_Spring2017_syllabus.pdf
├── README.md
├── Tutorials.Rmd
├── Tutorials.html
├── index.Rmd
└── index.html

1 directory, 16 files

```





```

```



------
<div id='id-section5'/>
### Page 5: 2017-01-30. Week 3, Day 4, class notes , Group presentations of project ideas



Melissa gave handoout for a general formula. This may help articulate and motivate and objectives  of the eco genom project. this approach can be applied to your other research projects, papers, or grants!



1. **The opener:** capture the attention of your audience highlighting an important area of research
2. **Current knowledge:** What is known about this area and will facilitate your work? 
3. **The Gap statement:** Where is the gap in the understanding? The critical missing bit of knowledge that prevents forward scientific progress? 
4. **Objectives:** Articulate the objectives of your research- "Here we..."
5. **Central hypothesis:** null and alternative 
6. **How will you test this hypothesis?** How will you distinguish between alternative explanations, will you have the statistical power to do so? 
7. **What are your expected results/outcomes?** 



Steve will be writing up projects on the board: 

1. **Immune-related gene expression** 
   * reverse pathology
   * looking specific classes of genes
   * a priori tests for resistance genes
     * compare individuals that stayed healthy vs those that got sick
     * looking at S-H transition 
   * **Group(Name = Sherlock):** Erin, Sam, Alex, Lauren, Dr. Brody, and 
     * Interested in reverse pathology
     * What type of pathogens are causing immune response differences? 
       * Viral specific, fungal specific, or bacterial specific
       * Focus on the transitions: HS, HH, SS
         * blocking based on time 
         * what is the workflow? 
           * ​
     * Back up Q: comapre responses to another species. 
     * Use random group of genes to use as housekeeping and control
     * make heat map or venn diagram of differential gene expression 
     * ​
2. **Intertidal vs subtidal** 
   * Genetic differences in susceptibility
   * local adaptation? 
   * gene expression differences
   * **Group discussion(Name=):** Lauren, Laura, Kattia, Dr. K
     * subtidal more susceptible than intertidal. What differences contribute to that? 
     * Focus on GXP expression between the two groups: ID, genes that are more diff expressed and do a functional enrichment analysis (immune vs general stress response; tease apart handling and susceptibility)
     * Focus on community structure of micro biome between the two groups: subtotal = more diversity? Equals more resilient to pathogen? Specific taxa associated with disease? 
       * Candidate genes in stress response? They want to do  a broad survey of genes (generalized). 3 broad categories: **stress, immune, other**. 
       * Time point? Use first time point (day3 ); potentially comparing healthy vs sick 
       * Not looking at SNP level differences 
       * Potentially associate gxp with micro biome ; mantel test. 
3. **Temporal Variation** 
   * chagnes in gene expression through time
   * changes in microbiome through time
   * temporal differences in H vs S
   * **Group discussion (Name=):**
     * change of gxp through time: compare HH vs HS (that made it to day 15)
       * ignore SS 
       * for each time point, what genes are differentially expressed between HH and HS
       * ID'ing those genes 
     * What is causing sickness? and how organisms are affected by it?(this is focus)
     * stability of gxp for HH vs HS; House keeping genes? 
     * Which ones are varying over time? 
     * **functional enrichment for varying or stable through time**
     * ​
4. **Heritability of microbiome**
   * compare microbial commuity to host individual relatedness
5. **Comparison within the intertidal group**
   * genetic differences ( 3 gropus of individual)
   * delta in microbiome
   * **Group discussion (Name=Rising starfish ):**
     * Intertidal group only: control for the handling stress
     * Want to do is access genomic differences (SNP data) between individuals that stayed healthy. HH, vs Sick
       * Differences between intertidal and subtidal 
     * Genetic basis with respect to susceptibilty 
     * Look at micro biome: microbiome composition of Healthy vs Sick
     * Microbiome changes across each time point for all of the individuals 
     * one specific group of microbes that are found in healthy that are lacking in the sick(indicator taxa)
       * aides in resilience or susceptibility 
     * Thinking about all time points(or we can start first day) 
     * How many OTUs? > 100s
     * Rare taxa might drop out? 
     * check allele frequency differences among sick and healthy 



### Admin stuff



**Logging into the cluster:** 



```
ssh adnguyen@pbio381.uvm.edu
```



Going in to the root: 



```
[adnguyen@pbio381 ~]$ cd /
[adnguyen@pbio381 /]$ ls
autorelabel  boot  dev  home  lib64  mnt  opt   root  sbin  sys  users  var
bin          data  etc  lib   media  nsr  proc  run   srv   tmp  usr
```



Stuff is stored on the data/ directory.  Let's look inside

```

[adnguyen@pbio381 /]$ cd data/
[adnguyen@pbio381 data]$ ls
databases     packages  project_data  temp_data
example_data  popgen    scripts       users

```

**Notes**: Stuff that needs to be installed, goes into the popgen folder



### Repeated measures anova or time series of differential gene expression 

We need to figure out how to do this. 





------
<div id='id-section6'/>
### Page 6:
------
<div id='id-section7'/>
### Page 7:
------
<div id='id-section8'/>
### Page 8:
------
<div id='id-section9'/>
### Page 9:
------
<div id='id-section10'/>
### Page 10:
------
<div id='id-section11'/>
### Page 11:
------
<div id='id-section12'/>
### Page 12:
------
<div id='id-section13'/>
### Page 13:
------
<div id='id-section14'/>
### Page 14:
------
<div id='id-section15'/>
### Page 15:
------
<div id='id-section16'/>
### Page 16:
------
<div id='id-section17'/>
### Page 17:
------
<div id='id-section18'/>
### Page 18:
------
<div id='id-section19'/>
### Page 19:
------
<div id='id-section20'/>
### Page 20:
------
<div id='id-section21'/>
### Page 21:
------
<div id='id-section22'/>
### Page 22:
------
<div id='id-section23'/>
### Page 23:
------
<div id='id-section24'/>
### Page 24:
------
<div id='id-section25'/>
### Page 25:
------
<div id='id-section26'/>
### Page 26:
------
<div id='id-section27'/>
### Page 27:
------
<div id='id-section28'/>
### Page 28:
------
<div id='id-section29'/>
### Page 29:
------
<div id='id-section30'/>
### Page 30:
------
<div id='id-section31'/>
### Page 31:
------
<div id='id-section32'/>
### Page 32:
------
<div id='id-section33'/>
### Page 33:
------
<div id='id-section34'/>
### Page 34:
------
<div id='id-section35'/>
### Page 35:
------
<div id='id-section36'/>
### Page 36:
------
<div id='id-section37'/>
### Page 37:
------
<div id='id-section38'/>
### Page 38:
------
<div id='id-section39'/>
### Page 39:
------
<div id='id-section40'/>
### Page 40:
------
<div id='id-section41'/>
### Page 41:
------
<div id='id-section42'/>
### Page 42:
------
<div id='id-section43'/>
### Page 43:
------
<div id='id-section44'/>
### Page 44:
------
<div id='id-section45'/>
### Page 45:
------
<div id='id-section46'/>
### Page 46:
------
<div id='id-section47'/>
### Page 47:
------
<div id='id-section48'/>
### Page 48:
------
<div id='id-section49'/>
### Page 49:
------
<div id='id-section50'/>
### Page 50:
------
<div id='id-section51'/>
### Page 51:
------
<div id='id-section52'/>
### Page 52:
------
<div id='id-section53'/>
### Page 53:
------
<div id='id-section54'/>
### Page 54:
------
<div id='id-section55'/>
### Page 55:
------
<div id='id-section56'/>
### Page 56:
------
<div id='id-section57'/>
### Page 57:
------
<div id='id-section58'/>
### Page 58:
------
<div id='id-section59'/>
### Page 59:
------
<div id='id-section60'/>
### Page 60:

------
