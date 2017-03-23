
------

<div id='id-section1'/> 

### Page 1: 2016-07-18. Ecological genomics, first class

### **Steve and Melissa's intro**    
*  Steve: It is a young field, trying to establish it's own identity    
   * Ecological genomics institute, KSU: emphasis on adaptation to environment   
   * Gordon Research Conference: Integrating different levels of biological organization on **ANY SYSTEM**; approach and tool focused! Field going towards new data and new analytic techniques  
   * Intro to eco genomics, oxford press; Using technology to address ecological issues such as nutrient cycling, population structure, life history vairation , trophic interaction, stress responess, and adpatation to environmental change   

*  DATA driven: next gen sequencing revolutionizes biology
   * creats a new problem--large datasets!!! how to make sense? 
   * not data limited and potentially computationally limited   

*  Where is the field headed    
   * Molecular Ecology Journal(flagship journal representative o the field)  
      * ALL systems:  corals, protists, daphnia, coral, lemurs, dandelions, steve studies trees 
      * model organism constraint disappearing!   
   * What types of questions are asked?  
      * How do genes correspond with circadian rythm?  
      * How does the microbiome influence the organism? 
      * How does epigenetic variation influence evolutionary responses? or contribute to phenotypic variation?  
      * What are the patterns of genetic diversity that can give us insights on population dynamics?  
      * What are constraints and tradeoffs and genetic mechanisms of traits? 

*  Methods?   
   * De novo genome assembly; sequencing a DNA book from scratch!!    
     * RNA-seq; transcriptomic profiling     
   * 16 s metagenomic sequencing      
   * Rad-seq/GBS for estiamting population structure and genetic diversity     

*  Proccesses studied?    
   * All evo and eco stuff; speciation, hybridization, local adaptation, genetic basis of local adaptation, genetic architecture of complex phenotypes, genes controlling host-pathogen evolutionary dynamics, pop structure, gene flow, epigenetics     

*  Goals of the course!    
   1. Learn how ecology and genomes shape each other   
   2. Think creatively about major questions, and pose testable hypotheses to those questions using appropriate genomic data    
   3. Think about careful experimental design and statistical analysis---shown by reading papers   
   4. Achive working knowledge and level of comfort for bioinformatics routines for ecological genomics studies   
      `'
   ### Melissa background  

**Background, what drove Melissa and Steve to ecological genomics?**       

Melissa read a cool paper that scales from analyzing a few loci to the whole genome.   

One figure popped out at her, FST (developed by Sewell Wright) histogram.   FST of 1= complete differentiation, FST of 0 = no diff. FST described as **Alleles in space**. From this histogram, Melissa was struck by how you can separate out neutral from selective ones.  

Melissa has a data set with 96 sea stars and then the 16s microbiome. Would be cool to see if there is heritability in some bactera
'
### Steve background   

* Inspired by Yanis Antonivics (an **OG**)   
* At the time, just so stories: **Adaptatationist programme**    
  * Just go out and go by feeling in a natural history way and prescribe an adaptation story   

* Janis wrote a creed to quantify the operational relationship between traits, environment, and genetics     
  * Yanis was on Steve's committee and Steve was interested in adaptation with respect to invasion biology because organisms need to respond to novel environments     * Phenotypes can relate to the environment, but what is the genetic basis of local adaptation (in situ)? There are other confounding issues: demographic effects, plasticity     
  * Steve thinks about environment-phenotype-genetics triangle. Basically a path diagram that feeds back on each other.    * Relationship between genes and phenotype ---GWAS (Genome wide association study)    
  * Relationship between genetics and environment --- Fst, clines between allele frequencies and environment    
* Invasion history is tough because of demographic history    
* He decided to focus on trees; large population size, straddle huge environmental gradients so the opportunity for selection is high   
  * positive relationship between Growing season length and traits    
  * Did a  reciprocal transplant of different populations to identify the extent of local adaptation in large established common gardens    
  * SK does GBS (genotype by sequencing)      
  * Problem with field: validating key gene candidates       


------

<div id='id-section2'/> 

### Page 2: 2017-01-19. Notes from papers discussed in class on 2017-01-23.
------

<div id='id-section3'/> 

### Page 3: 2017-02-01. Notes on from PuTTY command practice on 2017-02-01.   
I am going to make a new directory called scripts:   

    cd ~/     
    mkdir scripts   
    ll   

I opened the ~/ directory and it shows both mydata and scripts directories; good!   

    cd scripts    
    ll   

When I open scripts it showed nothing inside...totally as it should be   

Now I am going to move trim_example.sh to my scripts directory   

    cd ~/mydata   
    mv trim_example.sh scripts   
    cd ..   
    cd scripts   
    ll   

It wasn't there so I'm going to try again   

    mv trim_example.sh ~/scripts   

It said "no such file"; now there is no "trim_example" but there is a file called "scripts" so I might have renamed it?   

    head scripts   

Yup I accedentally renamed it; so I'll name it back to "trim_example" and then move it   

    mv scripts trim_example.sh   

Succesfully renamed! NOW I'm going to move it to scripts   

    mv trim_example.sh ~/scripts   
    cd ..   
    cd scripts   
    ll   

Its there! phew haha.  Now i'm going to move ssw_samples.txt from the server /data/project_data/ folder to my personal directory (~/mydata)  

    cd /data   
    cd project_data/   
     cp ssw_samples.txt  ~/mydata   
    cd ~/mydata   
    ll   

Its there!   From the ssw_samples.txt file I will create a HHonly and SSonly file.  First the HHonly:

    grep 'HH' ssw_samples.txt   
    grep 'HH' ssw_samples.txt >ssw_HHonly.txt   
    ll   
    head ssw_HHonly.txt   

Success!  Now the SSonly file:   

    grep 'SS' ssw_samples.txt >ssw_SSonly.txt   
    ll   
    head ssw_SSonly   

Success again!  Now we are going to move these two files to a new directory which we first need to make:

    mkdir sample_by_disease   

Great! now to move the files:

    mv *only.txt sample_by_disease/   
    ll   
    cd sample_by_disease/   
    ll   

It worked!   That will be all for today. =) 

------

<div id='id-section4'/> 

### Page 4: Notes from command line practice 2017-02-06; fastq files  
First thing: we will look at the fastq files in the server directory:   
```   
cd /data   
ll   
cd project_data/   
ll   
cd fastq   
ll   
```
gz=zipped    
file name = ```07_5-08_S_1_R1```
* 07 = individual   
* 5-08 = date   
* S = healthy/sick (sick)   
* 1 = degree of health from 0-5   
* R1 and R2 indicate left and right read (since it was paired reads)   

I will work on files:    
* ```15_5-17_S_3_R1.fq.gz```   
* ```15_5-17_S_3_R2.fq.gz```   

Unzip them with "zcat"  (ex: zcat FILENAME | head)   
```   
zcat 15_5-17_S_3_R1.fq.gz | head   
zcat 15_5-17_S_3_R2.fq.gz | head   
```
This is what it looks like when you unzip:   
```   
@J00160:  
63:  
HHHT2BBXX:1:1101:  
26839:  
1261 2:N:0:TCCGGAGA+AGGATAGG
CGGCTACCACATCCAAGGAAGGCAGCAGGCGCGCAAATTACCCACTCCCGACACGGGGAGGTAGTGACGAAAAATAGCAATACAGGACTCTTTCGAGTTCC
+
AAFFFJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJ<JJJJJJJJJJJJJJJJJJJJJJJJFJJJJFJJAJJJJFJJJJJJJJJJJJJJJJJJJJFJFJAF
```
__1st line__: info on sequencer etc   
__2nd line__: actual sequence (should be 100base long)   
__3rd line__: +   
__4th line__: Quality scores for each base (link in tutorial will tell you what each means; J and K are good)   
* a quality score better then or equal to 30 is typically used; therefore you want to see letters in your quality score.      

Use program called "FastQC" to look at quality more systematically   
```   
cd /data/scripts/   
ll   
cp trim_example.sh ~/mydata/   
```
People put it in their scripts that they created last week but my computer was dead so I don't have one thats why I put it in "mydata" *see page 3 for updated location*   
```   
cd ~/   
ll   
cd mydata   
ll   
```
Its in there!  We were just checking if they file copied over   

**NOTE**: control C cancelles a command which is running   
```   
head trim_example.sh   
```
The above command shows you the first ten lines of that file   
```   
vim trim_example.sh   
i     
```
"i" allows you to start editing   

We are doing the trimomatic program then we will do data visulization   

Everywhere that there is the word "samp" or "yoursample" we should put in our sample name   

change path from:   
```   
 				 /data/project_data/rawreads/filtered/YourSample_R1.fq.gz \
                 /data/project_data/rawreads/filtered/YourSample_R2.fq.gz \
                 ~/cleanreads/"samp_R1_clean_paired.fa" \
                 ~/cleanreads/"samp_R1_clean_unpaired.fa" \
                 ~/cleanreads/"samp_R2_clean_paired.fa" \
                 ~/cleanreads/"samp_R2_clean_unpaired.fa" \
```
to   
```   
 				/data/project_data/fastq/YourSample_R1.fastq \
                 /data/project_data/fastq/YourSample_R2.fastq \
                 ~/cleanreads/"samp_R1_clean_paired.fa" \
                 ~/cleanreads/"samp_R1_clean_unpaired.fa" \
                 ~/cleanreads/"samp_R2_clean_paired.fa" \
                 ~/cleanreads/"samp_R2_clean_unpaired.fa" \
```
copy = CTL C    
paste = CTL V   
When done with edits it should look like:   
```   
				/data/project_data/fastq/15_5-17_S_3_R1.fq.gz \
                 /data/project_data/fastq/15_5-17_S_3_R2.fq.gz \
                 /data/project_data/fastq/cleanreads/"15_5-17_S_3_R1_clean_paired.fa" \
                 /data/project_data/fastq/cleanreads/"15_5-17_S_3_R1_clean_unpaired.fa" \
                 /data/project_data/fastq/cleanreads/"15_5-17_S_3_R2_clean_paired.fa" \
                 /data/project_data/fastq/cleanreads/"15_5-17_S_3_R2_clean_unpaired.fa" \
                 ILLUMINACLIP:/data/popgen/Trimmomatic-0.33/adapters/TruSeq3-PE.fa:2:30:  
10 \
                 LEADING:28 \
             TRAILING:28 \
             SLIDINGWINDOW:6:28 \
             HEADCROP:9 \
             MINLEN:35 \
```
We should have changed:   
* file names (samp/yoursample to 15_5-17_S_3_R1)   
* path (2 paths for input; 4 paths for output)   

To save:   
* Press esc   
* ":w" write   
* ":q" quit   
```   
:w    
:q    
```
You can combine commands with:   
```   
:wq   
```
 Now you can make your script exicutable; if it is already exicutable it will be green   

You can run your program by:   
```  
./trim_example.sh    
```
It will tell you "completed successfully" when done; will tell you % that "survived" etc    

What it looks like when you run:   
```   

TrimmomaticPE: Started with arguments: -threads 1 -phred33 /data/project_data/fastq/15_5-17_S_3_R1.fq.gz /data/project_data/fastq/15_5-17_S_3_R2.fq.gz /data/project_data/fastq/cleanreads/15_5-17_S_3_R1_clean_paired.fa /data/project_data/fastq/cleanreads/15_5-17_S_3_R1_clean_unpaired.fa /data/project_data/fastq/cleanreads/15_5-17_S_3_R2_clean_paired.fa /data/project_data/fastq/cleanreads/15_5-17_S_3_R2_clean_unpaired.fa ILLUMINACLIP:/data/popgen/Trimmomatic-0.33/adapters/TruSeq3-PE.fa:2:30:  
10 LEADING:28 TRAILING:28 SLIDINGWINDOW:6:28 HEADCROP:9 MINLEN:35
Using PrefixPair: 'TACACTCTTTCCCTACACGACGCTCTTCCGATCT' and 'GTGACTGGAGTTCAGACGTGTGCTCTTCCGATCT'
ILLUMINACLIP: Using 1 prefix pairs, 0 forward/reverse sequences, 0 forward only sequences, 0 reverse only sequences
Input Read Pairs: 2016797 Both Surviving: 1721399 (85.35%) Forward Only Surviving: 216190 (10.72%) Reverse Only Surviving: 35588 (1.76%) Dropped: 43620 (2.16%)
```
* **ILLUMINACLIP** = its finding the adaptors and triming them    
* **SLIDINGWINDOW** = 6:28 = across 6 nucleotides...   

The link to the program website will tell you what each command within the "trim_example" file means  
```   
fastqc 15_5-17_S_3_R1.fq.gz   
```
Says that this file dosen't exist.  is that because i'm giving the command from the wrong folder   

I tried again in the "/data/project_data/fastq/" place and it worked.   

Now to move our html file to our computer:
```   
scp hlachanc@pbio381.uvm.edu:/data/project_data/fastq/15_5-17_S_3_R2.fastqc.html .   
```
Says no such file/directory; I suppose I'll try again later? It looks like the file is there

I decided to try running this command while I was in the directory with the fastq files (/data/project_data/fastq):   
```   
scp hlachanc@pbio381.uvm.edu:/data/project_data/fastq/15_5-17_S_3_R1_fastqc.html .
```
IT worked! =D   
Now I just need to figure out how to open it...   

In the mean time I decided to run the Fasqc for the R2 of my sequence:   
```   
fastqc 15_5-17_S_3_R2.fq.gz   
```
It ran succesfully however I'm not going to copy the html until I understand why we are doing that





------

<div id='id-section5'/> 

### Page 5: Notes from command practice in class 2017-02-08; Fastqc and winscp

```   
cd /data/project_data/fastq/cleanreads   
```
Now I need to run fastqc on each of the 4 files trimomatic generated and put into "cleanread" directory   
```   
fastqc  15_5-17_S_3_R1_clean_paired   
```
Didn't work. tried this:   
```   
fastqc 15_5-17_S_3_R1.fq.gz_clean_paired   
```
Didn't work   
```   
fastqc 15_5-17_S_3_R1_clean_paired.fa   
```
This worked   

Run FASTqc for the other three   
```   
fastqc 15_5-17_S_3_R1_clean_unpaired.fa   
```
Worked   
```   
fastqc 15_5-17_S_3_R2_clean_paired.fa   
```
Worked   
```   
fastqc 15_5-17_S_3_R2_clean_unpaired.fa   
```
Worked   

Go to winscp and move the 4 html files from cleanreads to your desktop and then open them to view the report   

In the report you will see green yellow and red icons off to the side.  They mean its good iffy and warning it might be bad   

Now we will use trinity to do some assemblies: start with two assemblies to compare   

You usually want the "paired" file that trimomatic generated when doing assemblies   

We will do an "experiment" to see how the transcriptom assembly can varry between individuals, H vs S etc   

Experiment we choose was to look at H vs S in the same individual (individual 19, H vs S)   
```    
Trinity --seqType fq --left(r1 paired) reads_1.fq --right(r2 paired) reads_2.fq --CPU 6 --max_memory 20G    
```
We will run this next week   

Screen is a command you can run that will let you run commands while you aren't logged on; good for commands that take a while.    

In trinity there is trinity stats that let you see #genes, contig legths, etc   

We will continue with mapping reads on Monday   

------

<div id='id-section6'/> 

### Page 6: Notes from command practice in class 2017-02-13; bwa aln 

The general work flow:   

1. Clean and evaluate reads (.fastq)  
   - we used trimmomatic    
2. Make and evaluate a transcriptome assembly (.fasta)  
   - we were going to do an experiment but ran out of time so looked at cleaned assembly (run with Trinity); results at the bottom of the tutorial for 2-6-17 (add link)   
3. Map cleaned reads to the transcriptome assembly (makes .sam files)   

From these sequence alignment files, we can extract two types of information:    

- (a) read counts - the number of reads that uniqely map to each “gene”   
- (b) single nucleotide polymorphisms between a sample and the reference
  ​    

With these two types of data, we can go on to differential gene expression analyses and population genomics.   

"Open reading frames": allow us to say We want complete transcripts and we want the longest one   

- She already did **Transdecoder** (only needs to be done once so we don't need to run it); how she ran it is on the tutorial (add link to tutorial here)   
- She started a **blast run** (which is probably done now)

Options for improving this assembly include:   
(1) using more reads from other individuals or trying a different individual   
(2) changing the cleaning and assembly parameters. We can evaluate based on the percentage of genes that have good blastp hits and the percentage of single copy orthologs included in the reference (for example using the new program BUSCO.)   

- She created **reference transcriptome** which we will compare ours too (will save us time)   
  - This is common; pick an individual to create a reference transcriptome and then compare the rest to it   
  - She used individual 15 for the reference transcriptome (complied all the time points etc to make one transcriptome for that individual)  
- Trinity.fasta = the results from that individual

```
#!/bin/bash/
cd /data/popgen/databases/
makeblastdb -in uniprot_sprot.pep -dbtype prot -out uniprot_sprot
blastp -query /data/project_data/assembly/Trinity.fasta.transdecoder_dir/longest_orfs.pep  -db /data/popgen/databases/uniprot_sprot  -max_target_seqs 1 -outfmt 6 -evalue 1e-5 -num_threads 10 > blastp.outfmt6
```

"makeblastdb" sets up the data base you will blast to so you can blast in here   
"These transcriptome assembly processes are ongoing. But for now we will map to the 5,693 “genes” based on the longest ORFs"   

**NOW** I will start doing commands:   

```
cd /data/scripts/
ll
cp bwaaln.sh ~/scripts
cd ~/scripts
ll
```

Its in there!  We just copied the file bwaaln.sh to my personal scripts folder   

Next we will edit the file and insert our left read file name:   

```
vim bwaaln.sh
i 
```

go to "my left" and switched it with 15_5-17_S_3_   

NOTE: she renamed our files   

```
myRight=${15_5-17_S_3_R1.fq.gz_left/_R2.fq.gz_right}
```

This file (bwaaln.sh) tells it that my left = my right   
echo is a program that prints to screen   

```
myShort=`echo $myLeft | cut -c1-11`
```

This command says to print "my left" to this cut function and tell it to cut the first 11 digits   

Indexing step (only needs to happen once; already done)   

use this bwa aln program   
Opened new putty window and ran:   

```
bwa aln
```

It gives you a list of all the areas you can control; we used defult perameters   

it will run the bwa aln on your left...:   

```
bwa aln /data/project_data/assembly/longest_orfs.cds /data/project_data/fastq/cleanreads/$myLeft > $myLeft".sai"
```

...And your right files:   

```
bwa aln /data/project_data/assembly/longest_orfs.cds /data/project_data/fastq/cleanreads/$myRight > $myRight".sai"
```

and generate a few file (ending in ".sai")   
Then it will run the last command which will create a combined aligned file:   

```
bwa sampe -r '@RG\tID:'"$myShort"'\tSM:'"$myShort"'\tPL:Illumina' \
        -P /data/project_data/assembly/longest_orfs.cds $myLeft".sai" $myRight".sai" \
        /data/project_data/fastq/cleanreads/$myLeft \
        /data/project_data/fastq/cleanreads/$myRight > $myShort"_bwaaln.sam"
```

We go from two cleaned files -> two intermediate files (.sai) to one combined file (.sam)   

To run this file:   

```
bash bwaaln.sh >> bwaoutput.txt
```

After it ran I opened the text file to see what was in there; it was just the file names that the file told to "echo" or print to screen   

My .sam file saves to the directory I ran the script in (~/scripts)   

```
cd ~/scripts/
ll
```

It is there!   
**BUUUT** it was wrong so I need to run the script again:   

I went back into the bwaaln.sh file and changed THIS:   

```
myLeft='15_5-17_S_3_R1.fq.gz_left_clean_paired.fq'
```

Instead the my left here:   

```
myRight=${myleft/_R1.fq.gz_left/_R2.fq.gz_right}
```

Once I edited the file I ran it again:   

```
bash bwaaln.sh
```

It ran   

```
ll
```

The new file has the right name! =D   

**HELPFUL TRICK**:     

To have it continue to run a command and close your screen:      

```
screen
```

To resume the screen that you detached from:   

```
screen -r
```



------

<div id='id-section7'/> 

### Page 7: Notes from command practice in class 2017-02-15; SAM file

**Coding outline:**

1. lab notebook (how to put notes into git hub)
2. SAM files
   1. Extract expression
3. What's going on in the background

**No class on Monday 2/20**

**Lab Notebook:**

1. Need: Typora and notebook.md (in github)
2. open temp in Typora
   - edit (use md cheat sheet)
   - save
3. Go to github desktop repository (repo)
   - commit to master
   - sync
4. Check that it is updated online



*Andrew's office hours:* **Friday 3-5pm**



*NOW* we will start coding

Go to your SAM file:

```
cd scripts
ll
```

SAM file is in there!

Next, save the last 100 lines:

```
tail -n 100 15_5-17_S_3_bwaaln.sam > tail.sam
vim tail.sam
:set nowrap
```

For some reason my SAM file ***didn't run all the way*** so I opened Melissa's file so I could follow along

```
cd /data/project_data
cd fastq
cd cleanreads/test
vim tail.sam
```

It should look like this:

```
J00160:  
63:  
HHHT2BBXX:4:2228:  
7953:  
48931   77      *       0       0       *       
J00160:  
63:  
HHHT2BBXX:4:2228:  
17655:  
48931  77      *       0       0       *       
```

The "77' (second column) is your SAM FLAG which you can check what it means by inserting the # into the flag decoder provided on the tutorial

Here is a list of what each column means in the SAM file:

- **1st column:** the read, aka. query, name,
- **2nd column:** a FLAG (number with information about mapping success and orientation and whether the read is the left or right read),
- **3rd column:** the reference sequence name to which the read mapped
- **4th column:** the leftmost position in the reference where the read mapped
- **5th Column:** the mapping quality (Phred-scaled)
- **6th column:** a CIGAR string that gives alignment information (how many bases Match (M), where there’s an Insertion (I) or Deletion (D))
- **7th column:** an ‘=’, mate position, inferred insert size (columns 7,8,9)
- **8th column:** the query sequence and Phred-scaled quality from the FASTQ file (columns 10 and 11)
- **9th column:** then Lots of good information in TAGS at the end, ***if the read mapped***, including whether it is a unique read (XT:A:U), the number of best hits (X0:  
i:1), the number of suboptimal hits (X1:  
i:0).

example:

```
 RG:Z:38_6-24_S_5        XT:A:U  NM:i:0  SM:i:37 AM:i:0  X0:  
i:1  X1:  
i:0  XM:i:0  XO:i:0  XG:i:0  MD:Z:89
```

The BWA man page (link on tutorial) shows you what each TAG means

Use the grep command to tell you how many reads mapped uniquely

```
grep -c XT:A:U 38_6-24_S_5_bwaaln.sam
```

I got 1177827   

above looks at XT which is unique (see BWA man page for more detail)

also try this one:

```
grep -c X0:  
i:1 38_6-24_S_5_bwaaln.sam
```

I got 1182952   

The first grep command seemed to be the better indicator of the # of uniquely mapped reads

Go and find the python script:

```
cd /data/scripts
ll
```

Copy the python script to where your sam file is:

```
cd /data/scripts
cp countxpression_pe.py ~/scripts
python countxpression_pe.py 20 35 countstatssummary.txt YOURFILENAME.sam
```

This python script will take the sam file and make a list of the genes and counts how many reads uniquly mapped to each gene 

We are running:

```
sed -i 's/::/\_/g' yourfile.sam 
```

This lets you change something within your file:

​	s = search
​	:: = find this
​	_ = replace with this
​	g = globally 

This python can take a while so run in 'screen'

When you open the count file we are interested in the first column

- **1st column** # of unique reads


- **2nd column** # reads that mapped to this gene *and* other genes
- **3rd column** # reads total (unique + mapped to other genes)

2 files generated from python: countoutout; countstatssummary

*only 7.4% were quality aligned (thats why we need a better assmebly which will be done by Melissa before next class)





------

<div id='id-section8'/> 

### Page 8: Notes from command practice in class 2017-02-22; working in R

#### **Make sure you have:**

- R
- R studio
- DESeq downloaded in R studio (copy commands from bottom of tutorial from last class)
- move files from /data/project_data/DGE to your computer (use WinSCP)
  *(I saved them to a folder on desktop called "class 2-22 files for R")
  -open "DESeq2_exploreSSW_trim.R" in R studio  (simply go to: file -> open file -> then open this file)

#### **Other Notes:**

- Melissa made a new transcriptome assembly (since our previous mapping was not great)
- Melissa made assembly on server (hard because it has limited memory)
- these are reads that are mapping to the assembly
- final assembly 26000 genes
  D- countdata_trim.txt has only some of the samples (allcounts data file not up yet but it wil have all samples)

### **Working in R**

- how to run code (2 ways):
- have your cursor in the line you want to run then hit "CTL R"
- highlight and run



Thus far (lines 12-41) we have looked at data that we already had; we havent generated any new data yet

- first data we generate is when we run "dds <- DESeq(dds)..."



Overall our assembly is still not great (better but still lots of low counts)



**plotMA**

- Above: highly expressed and healthy
- Below: highly expressed and sick



**Interaction maps:** (around lines 145)

- 1 gene

- healthy and sick; intertidal and subtidal

- y axis: normalized read counts 

  ​

**Issues with line 97 (scale for y...)



Melissa will try to improve mapping again by Monday (so we can BLAST)

------

<div id='id-section9'/> 

### Page 9: Notes from command practice in class 2017-02-27; DESeq models 1-3 in R

## Coding session:

<<<<<<< HEAD
1) move new data    
​	moved all the data from DGE to my desktop by using winSCP to drag and drop   
​		stored them in folder on desktop called "DGE data from 2-27"    
2) DESeq2 (5 models)   
3) your models   

=======
1) move new data 
​	moved all the data from DGE to my desktop by using winSCP to drag and drop
​		stored them in folder on desktop called "DGE data from 2-27" 
2) DESeq2 (5 models)
3) your models



## Begin coding

open R (open script in R or double click file to open)   

*Andrew suggested randomly sampling the data; we will sample 10% of data using random sampling function     


***1st homework:*** setting up differently expression analysis; this will be practice for that   

=======
***1st homework:*** setting up differently expression analysis; this will be practice for that



### Model #1 (TEST EFFECT OF HEALTH CONTROLLING FOR LOCATION); Lines 18-81

```
Ran commands from line 1-13 all at once
```


**Line 1:** change this to be a directory on your computer   

**Lines 2 and 4** loads programs   

=======
**Line 1:** change this to be a directory on your computer

**Lines 2 and 4** loads programs

**Lines 6-8** preparing and checking data to be used in R

**Line 6:** opened the new "contsdata_trim2" file
​	*header* = true; first line is header
​	*strings as factors*; letters = factors not numbers
​	*row.names* = 1 there are names in this row 

**Line 7:** load meta data 
​	*as.matrix* stores it as an r object converst into data matrix form

**Line 8:** look at head of data to check


**Line 18:  
** dds <- DESeqDataSetFromMatrix(countData = countData, colData = colData, design = ~ location + health)    
​	it wants: count daa, col data, and design   
​	we created count data and col data files earlier (lines 1-13)  
​	*Desgin is important; here we are looking at **health** as the MAIN EFFECT   
​	this will test for an effect of the last term while controling for an effect of the other term(s) listed  
​	We are: testing health while controling for differences in location  
​	trying to remove variance of location and then testing variance of health   
​	*if you wanted to test for health in general you can delete location and only type in "health"  
​	trying to remove variance of location and then testing variance of health   

***NOTE:*** all plot commands are at the bottom  
​	at any point you can look at a plot of your data but you will need to change the conditions  
=======

**Line 18:  
** dds <- DESeqDataSetFromMatrix(countData = countData, colData = colData, design = ~ location + health)
​	it wants: count daa, col data, and design
​	we created count data and col data files earlier (lines 1-13)
​	*Desgin is important; here we are looking at **health** as the MAIN EFFECT
​	this will test for an effect of the last term while controling for an effect of the other term(s) listed
​	We are: testing health while controling for differences in location
​	trying to remove variance of location and then testing variance of health 
​	*if you wanted to test for health in general you can delete location and only type in "health"
​	trying to remove variance of location and then testing variance of health 

***NOTE:*** all plot commands are at the bottom
​	at any point you can look at a plot of your data but you will need to change the conditions


```
Run line 18 then line 26
```

shows 13053 (number of genes in transcritome assembly that we mapped to) 77 (number of samples)



**Line 29:  
** says it needs at least 100 reads to make it valid



```
Run lines 29 and 30
```

It shows: 12954 (number of genes in transcritome assembly that we mapped to) 77 (number of samples)  
​	Means that about 100 genes (13053-12954) that didn't have any reads  
​	only losing 100 is much better then our last class assembly   

**Line 35:  
** this randomly chooses 1200 rows from our 12000 so we can have a smaller set to work with when running the models next  
​	***NOTE:*** THIS IS FOR **PRACTICE ONLY** normally you would want to run all

**Line 38:  
** by putitng "H" first we are saying the healthy are the set to which we should compare

```
Run lines 35, 36, 38 and 40
```

**Line 43:  
** sorts by p value so you can look at top 6 significant genes

**Line 45:  
** "# log2 fold change (MAP): health S vs H"  since the S came first it is the "up" one in summary results

```
run lines 42, 43, 44
```

**Line 73:  
** does a summary of what we just ran (res; aka resutls)
shows that LFC going up (sick) has 24 genes that were more highly expresssed in sick vs healthy; and LCF (log fold change) going down (healthy) has 8 



### Model #2 (interactions); Lines 86-142

*Basically this is very simliar to model #1 but we added the new interaction and we are using more cores to process the data (parallel)

**line 86:  
** same as line 18 except design has a new interaction added "location:health"

**line 97:  
** "parallel" uses two cores of your computer to run the script (goes faster)

```
run lines 86-100
```

gives you "# [1]  "Intercept"           "location_sub_vs_int" "health_S_vs_H"       "locationsub.healthS""  
​	just shows locationsub interacting with healthyS but her understanding is it is running all versions of interactions  
​	only showing results names at this point   



***NOTE:*** if you ever have a question about a command you can seach the DEseq tutorial or type "?command"



```
Run lines 103,104,105,134
```

Shows that the more factors you use you might miss picking up certain data; therefore do lots of models and compare

**To save results:** command not in this script but you can look up in tutorial; might also be in 1st version of script

can have it show you only significant; "res 
<- res[order(res$padj> 
0.05),]" (something like that; she will update to include



### Model #3 (GROUP DESIGNS can be used for contrasts of interest or interactions); lines 147-198

**Line 147:  
** set up what groups you want (location, health)

**Line 148:  
** desing is "group" lumps all possible groups (for variables that you specificed in the line above) into a group

**Line 159:  
** shows you the groups

**Line 163:  
** sets up what groups you want to contrast; here we contrast inter vs sub at various healthy and sick levels

**Benefit of group; lets you focus on specifc variables (inter vs sub, day, etc)

------

<div id='id-section10'/> 

### Page 10:  
 Notes from command practice HOMEWORK 2017-02-28; DESeq models 4-5 in R

**HOMEWORK:** Finish running through the DESeq2 script by 3-1-17
We had completed running model 3 therefore I have to do:

- model 4 (lines 204- 215)
- model 5 (lines 220-260)
- any plots at the bottom of the script

### Model 4 (TIME SERIES USING REDUCED MODELS); lines 204- 215

Start by loading the programs again (run lines 2 and 4)

Looks similar to the other models except:
​	**Line 204:  
** the command is "ddsTS" instead of "dds" and there is no "design" section.  command below for comparison

```
Model 4: ddsTS <- DESeqDataSetFromMatrix(countData = countData, colData = colData, ~ health + day + health:day)
Model 3: dds <- DESeqDataSetFromMatrix(countData = countData, colData = colData, design = ~ group)
Model 1: dds <- DESeqDataSetFromMatrix(countData = countData, colData = colData, design = ~ location + health)
```

Now I will try running line 204:  


```
Run line 204
```

It said, "Error 'countData' not found"
I went back and ran lines 6-13
This time it worked

**Lines 205, 207, and 208:  
** similar to lines 29, 35 and 38

```
run line 205 and 207 and 208
```

I link model 4 is really just looking at health vs day and the key spots you see changes to the commands are:

- line 204 (end of command)


- line 210 ("reduced = ~ health + day")

```
Run lines 210-215
```

Summary showed:

```
out of 1198 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)     : 0, 0% 
LFC < 0 (down)   : 0, 0% 
outliers [1]     : 16, 1.3% 
low counts [2]   : 2, 0.17% 
(mean count < 0)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

Is that correct?

### Model 5 (EFFECT OF DISEASE SEVERITY SCORE); Lines 220-260

Similar to other models but the desgin this time is "~ score"

```
run lines 220-262
```

After trying to run line 220 and got this message


```
the design formula contains a numeric variable with integer values,
  specifying a model with increasing fold change for higher values.
  did you mean for this to be a factor? if so, first convert
  this variable to a factor using the factor() function
```

Continued running the other commands anyways and ended with this:

```
out of 1196 with nonzero total read count
adjusted p-value < 0.1
LFC > 0 (up)     : 22, 1.8% 
LFC < 0 (down)   : 4, 0.33% 
outliers [1]     : 7, 0.59% 
low counts [2]   : 508, 42% 
(mean count < 12)
[1] see 'cooksCutoff' argument of ?results
[2] see 'independentFiltering' argument of ?results
```

seems similar to what she got in the script example.

Take aways:
​	I can run these models but I'm not sure what exactly they just did. (will ask quesstions in class)



Tried running a few **plots** but don't know enough about them to troubleshoot yet.  Will ask for help/try again later.   


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
