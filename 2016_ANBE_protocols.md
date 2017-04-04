# All lab protocols from temperature treating ants to quantifying gene expression    
### Author: [Andrew D. Nguyen](https://adnguyen.github.io/), PhD Candidate    
### Affiliation: University of Vermont      
Mentors/Advisors: [Dr. Sara Helms Cahan](http://shelmscahan.github.io/) and [Dr. Nick Gotelli](http://www.uvm.edu/~ngotelli/homepage.html)

Date Initiated: 20160324   

Last date modified: 2017-04-03     

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.    


# Table of contents    
- [Lab-acclimating ants](#id-section0)   
- [Workflow](#id-section1)   
- [Heat shock experiments](#id-section2)   
- [RNA isolations](#id-section3)
- [cDNA synthesis](#id-section4)
- [quantitative real time PCR](#id-section5)


<div id='id-section0'/>    

## Lab-acclimating ants     

**Lab-acclimation at 25 C in the [Gotelli lab!](http://www.uvm.edu/~ngotelli/homepage.html)**    
![](https://cloud.githubusercontent.com/assets/4654474/14787126/1b5cd0a4-0ad0-11e6-8a08-d818ba53d15a.jpg)   

 **Ants are reared in tupperware (22X16cm) containers**   
 They are housed in fluon-lined(insect-a-slip) containers so that they stay inside the tupperware. We fill in the container with sand and place mealworms and honey water for them to eat!     
 ![](https://cloud.githubusercontent.com/assets/4654474/14787149/2fcdadd8-0ad0-11e6-93ab-83a844e5fa7e.jpg)     

**They like living in water plugged tubes!**    
RO water is filled to about 1/3 of the water tube and plugged with a cotton (folded hot dog and then hamburger).   
![](https://cloud.githubusercontent.com/assets/4654474/14787139/29c182b6-0ad0-11e6-9bc4-af75bd9ec34f.jpg)


## Ant feeding:    
1. Take tops off, replace honey tray and meal worm half tray.    
2. Cut 1 meal in very small pieces and place on half tray (simply rip full tray in half).   
3. Make honey water solution (10%) and dispense ~ 100uL into honey tray.    
4. Clean area where you made honey water and where you cut meal worms.    

Notes:   
* If we run out of honey water, buy some at the Davis center and keep the receipt to get reimbursed ( or ask for money). 
* Visually inspect colonies while feeding to get rid of old water tubes. Make new water tubes if they need it.   


<div id='id-section1'/>    

## Workflow    

The workflow for my gene expression projects usually follows this trajectory:

1) Experimentally manipulate ants  (heat shocks typically); flash freeze and store at -80C until we need to quantify gene expression    
2) Homogenize (break up ants) in buffer and isolate RNA     
* Quantify with nanodrop or qubit    
  * If it's you're first time, check intactness of RNA with RNA analyzer (get RIN estimates)     


3) Convert (~50-100ng) RNA to cDNA      
4) Quantitative real time PCR    


<div id='id-section2'/>   

## Heat shock experiments     

There is a large discussion for how we should heat shock ectotherms: static (dunk at 1 temp) , dynamic (heating over time). I've done both. 

See these refs if interested:  
Pro static camp:     
* Rezende EL, Castañeda LE, Santos M. 2014. Tolerance landscapes in thermal ecology. Funct Ecol 28:799–809. (double check this ref; having it here so I'll read it)   
* Rezende EL, Tejedo M, Santos M. 2011. Estimating the adaptive potential of critical thermal limits: methodological problems and evolutionary implications. Functional Ecology 25:111–121.     

Pro slow ramp:     
* Terblanche JS, Hoffmann AA, Mitchell KA, Rako L, Roux PC le, Chown SL. 2011. Ecologically relevant measures of tolerance to potentially lethal temperatures. J Exp Biol 214:3713–3725.
* Overgaard J, Kristensen TN, Sørensen JG. 2012. Validity of Thermal Ramping Assays Used to Assess Thermal Tolerance in Arthropods. PLoS ONE 7:e32758.

### General Waterbath set up    

**Automated water bath**   
![](https://cloud.githubusercontent.com/assets/4654474/14787150/31ba1280-0ad0-11e6-9693-2a4158421275.jpg)

**Submerging ants in the waterbath**
![](https://cloud.githubusercontent.com/assets/4654474/14787105/033be3de-0ad0-11e6-8fbc-4f6703209086.jpg)

**Static heat shock:**    
**Notes:**     
Depending on organism, you might want to test out which temperature will give a loss in righting response (Knock down time)   
**Steps:**     
1) Set temperature on circulating water bath
 *Set temperature to internal probe of glass tube     

3) Placed ants in glass tubes (dimensions? ) and let ants equilibrate to stress for 5 minutes at room temperature.    
2) Dunked glass tubes with ants in pre-set water bath    

**Dynamic heat shock (ramping heat shock):**    
**Notes:**     
* We used a programmable circulating water bath from polyscience: 
  https://www.polyscience.com/products/circulating-baths/heated-circulators/integrated-heated-baths/performance-programmable-controller      
* It took us a while, but we ramped the water bath to an internal thermometer at 0.1 C / min     
* Glass tubes: WWR borosilicate glass tubes 16 X 150 mm ; https://us.vwr.com/store/catalog/product.jsp?product_id=4675780      

**Steps:**       
1) Place ants in glass tubes with cotton plug (so they don't escape) and let them equilibrate to stress for 5 minutes at room temperature     
2) Pre-set water bath to 25 C (their rearing temperature); set up internal probe in a glass tube     
3) Place glass tubes with ants in water bath     
4) Start ramping protocol which incubates the tubes at 25C for 5 minutes and then slowly ramps 0.1C/min; also start timer     
5) Measure knockdown  time (seconds)  and temperature ( degrees C); knockdown = loss of righting response, so if you flip them over, they can't get back up after 5 second     




<div id='id-section3'/>    

## RNA isolations    

This protocol outlines how I have isolated RNA with little short cuts that speed up this process

**Notes, reagents and supplies:**   
* I use the qiagen rneazy micro kit: https://www.qiagen.com/us/shop/sample-technologies/rna/rna-preparation/rneasy-micro-kit#orderinginformation    
* Depending on how accurate you want to quantify gene expression and budget, DNAse I treatment gets rid of potential DNA that can get picked up in a qPCR experiment. It comes with the Rneazy micro kit.      https://www.qiagen.com/us/shop/lab-basics/enzymes/rnase-free-dnase-set#orderinginformation    
* RNases are everywhere and can rapidly degrade RNA. We use BME to inhibit RNase activity. We add 10 uL of BME per 1 mL of RLT buffer (buffer we homogenize in ) http://www.sigmaaldrich.com/catalog/product/sigma/m7154?lang=en&region=US  
* 2mL Homogenizing tubes (Sarstedt, Germany? )  :  https://www.sarstedt.com/en/products/laboratory/screw-cap-micro-tubes-reaction-tubes/screw-cap-micro-tubes/product/72608/   
* Bullet Blender (NExt Advance)  http://www.nextadvance.com/product/bullet-blender-standard/
* 1.4 mm Zirconium silicate grinding beads (Quackenbush co., inc.) : http://www.quackco.com/qbzirc.htm
* Eppendorf repeater pro: http://www.pipettesupplies.com/store/parts/repeater-pro-eppendorf/   
* DONT touch the inside of the tubes    
* sterilize working bench with ethanol and bleach; lay down diapers. Use RNase AWAY: https://www.thermofisher.com/order/catalog/product/10328011      


**Steps for RNA isolation:**     
1) Set up all the tubes you need for the experiment      
* For each sample, I set out 3 X 1.5 mL eppendorf tubes and label them  
   * 1 tube for transfer ant homogenate
   * 1 tube for 70% ethanol 
   * 1 tube for eluting into

* Set up homogenizing tubes ( 1 tube per sample) 
   * Add 1 scoop of grinding beads 
   * Add 350 uL RLT with BME and RNA carrier ( add concentrations here)        


2)  More set up
* Make fresh 70% and 80% ethanol. I usually do this in a 15mL conical. Add 350 uL 70% ethanol into one of your 1.5 mL eppendorf tubes      
* Take out rneazy spin columns out of package and keep them refrigerated, label them      
* Prepare DNase I by adding 10uL DNase and 70uL RDD buffer together. Make master mix so you can add to all of your samples.    *DNase I is sensitive to mechanical forces and can denature!! Be careful in how you pipete        

3) Get liquid nitrogen and place samples(ants in 1.5mL tubes) into liquid nitrogen     
4) Quickly transfer tubes with ants from liquid nitrogen into homogenizing tubes (it has 350 uL of RLT buffer with BME and RNA carrier) and use bullet blender under highest settings for 1-3 minutes
* Pogonomyrmex barbatus usually takes 3 minutes and double the amount of grinding beads (2 scoops)
* Aphaenogaster usually takes 1 minute

5) Spin down for 30 seconds, highest rpms (~14,000g)     
6) Transfer supernatant into new 1.5mL tube; spin down 30 seconds, highest rpms       
7) Transfer supernatant into 1.5mL tube with 70% ethanol; mix; with same pipette, add ~700 uL into spin column (pink)      
8) Discard flowthrough; Spin 30 seconds, highest rpms       
9) Wash step: add 350 uL RW1 buffer and spin 30s highest rpms             
10) Add 80 uL DNAse 1; incubate 30 minutes at room temperature     
11) Wash step: add 350 uL RW1 buffer and spin 30s highest rpms; discard flow through tube and put column in a new one       
12) Wash step: add 500 uL RPE(previously added with 44mL 100% ethanol) buffer and spin 30s highest rpms
13) Wash step: add 500 uL 80% ethanol buffer and spin 30s highest rpms; put in new flow through tube   
14) Drying step: spin 5 minutes highest rpms    
15) Place column into 1.5 mL eppendorf tubes; add 17 uL water straight to the column; spin 10K rpms for 1 minute

**Quantify RNA** 
We have used two ways to quantify RNA: qubit and nanodrop   
* Qubit protocol: https://www.thermofisher.com/order/catalog/product/Q32852    
* nanodrop: http://www.nanodrop.com/    

Also, double check RIN values to check your technique. You can have high RNA concentrations but your RNA can be degraded. 
Rin values: http://www.genomics.agilent.com/article.jsp?pageId=2181&_requestid=268830

<div id='id-section4'/>
##cDNA synthesis
* We use the high capacity cDNA synthesis kit : http://www.thermofisher.com/order/catalog/product/4368813?icid=cvc-rt-rt-pcr-c1t1   
* I also like to use RNAseOUT to be doubly sure my RNA does not get degraded: https://www.thermofisher.com/order/catalog/product/10777019    
* I like using these pcr strip tubes: http://www.simport.com/products/pcr/pcr-strips/low-profile-amplitube-pcr-reaction-strips-t320-2lpn.html     


**Steps:**  
Notes: Everything should be done on ICE!   
These steps include samples + a negative control and -multiscribe control.    

1) Set up for 20 uL rxns: For each sample, add 50ng of RNA into a pcr strip tube into a final volume of 10 uL 
* ex:       


| Sample ID | Treatment    | Qubit/nanodrop Quantification (ng/uL) | uL sample for 50ng | nuclease free water to add | total volume |
| --------- | ------------ | ------------------------------------- | ------------------ | -------------------------- | ------------ |
| Ant1      | Heat shocked | 6.53                                  | 7.66               | 2.34                       | 10           |





2) Set up reaction, here is a typical set up; dont add anything yet, just set up master mix calculations       

**Table B for reaction set up for cDNA synthesis**        

| Reagent             | Inital conc.          | Final conc | uL to add 1rxn | 10 rxns |
| ------------------- | --------------------- | ---------- | -------------- | ------- |
| RT Buffer           | 10x                   | 1x         | 2              | 20      |
| dNTPs               | 25x or 100 mM         | 1x or 4 mM | .8             | 8       |
| RT Random Primers   | 10x                   | 1x         | 2              | 20      |
| Rnase inhibitor     | 5000 units(or 40U/uL) | 4 units    | 1              | 10      |
| RT Multiscribe      | 50 U/ uL              | 5 U/uL     | 1              | 10      |
| nuclease free water | na                    | na         | 3.2            | 32      |
| total               |                       |            | 10             | 100     |




3) I like to make a master mix with (# of samples + 4 rxns). So if you have 6 samples, make a master mix of 10  
4) Add everything except multiscribe (table B). Take 1 rxn out (9 uL) for -multiscribe control
5) Add mulitscribe to master mix ( but subtract a uL)
* So if you have a 10 rxm master mix, you took out 9 uL in step 3 and now add 9 uL of multiscribe beccause you have a 9rxn master mix now)    

6) Dispense 10 uL of master mix into tubes with your samples to reach 20 uL reaction      
7) PCR with following conditions:      
 1. 25 C, 10 min    
 2. 37 C, 120 min     
 3. 85 C, 5 min    
 4. 4 C, infinity    


8) Store -20C until you need to dilute for qPCR. Prior to qPCR, dilute cDNA 1/10.      


<div id='id-section5'/>    

## Quantitative real time PCR    

* Power Sybr green kit (ThermoFisher USA) : https://www.thermofisher.com/order/catalog/product/4367659      
* Thermocycler: ABI steponeplus; https://www.thermofisher.com/order/catalog/product/4376600     
* 96 well plates: https://www.thermofisher.com/order/catalog/product/4346907      



### Primer list ([design scheme](http://adnguyen.github.io/blog/2016/04/12/Primer_design))


| Gene                | Primer 5'-3'               | Amplicon Length (bps) |
| ------------------- | -------------------------- | --------------------- |
| 18s rRNA (forward)  | CTCTTTCTTGATTCGGTGGGTG     |                       |
| 18s rRNA (reverse)  | TTAGCAGGCTAGAGTCTCGTTC     | 100                   |
| GAPDH (forward)     | TAAGATTGCCGTCTTCAGCG       |                       |
| GAPDH (reverse)     | ATGCCTTCTCGATGGTTGTG       | 110                   |
| β-actin (forward)   | TAAGATTATCGCTCCACCCG       |                       |
| β-actin (reverse)   | CTCGTCGTATTCCTGCTTCG       | 112                   |
| Ef1-β (forward)     | GGTTCAGATGAAGAGGAAGATG     |                       |
| Ef1-β (reverse)     | TCATCTCCCCAACTTTTCAC       | 111                   |
| hsp83 (forward)     | AGTGCTACGAGCAATTCAGC       |                       |
| hsp83 (reverse)     | CGGATGCAGAAGTGTGATAACG     | 105                   |
| hsc70-4_1 (forward) | CTTAATGTCTCCGCCGTGGATAAG   |                       |
| hsc70-4_1 (reverse) | CTCAGCTTCGTTTACCATCCTCTC   | 115                   |
| hsc70-4_2 (forward) | GATCAAGAGGAACACGACGATACC   |                       |
| hsc70-4_2 (reverse) | GCTCTTTCTCCCTCATAGACTTGG   | 105                   |
| Bip(forward)        | GGTACAGTGATAGGAATTGATCTGGG |                       |
| Bip(reverse)        | TAAGAAGGCGTGATTCGGTTACC    | 112                   |
| hsc70-5 (forward)   | CGTTTAGTTGGTATGCCTGC       |                       |
| hsc70-5 (reverse)   | CAGGATCTTCAAATCTCCGTCC     | 100                   |
| hsp60 (forward)     | GTTGAAGAAGGAATCGTTCCCG     |                       |
| hsp60 (reverse)     | CGATCTTGATTCCAGTCTCCTG     | 109                   |
| hsp40 (forward)     | GATATGGATCCCTTTGGACTCG     |                       |
| hsp40 (reverse)     | CCCTTTACAAGTATTCGGACTCG    | 120                   |
| l2efl_#4 (forward)  | TTTCCGGAGTAAGCTCGTTC       |                       |
| l2efl_#4 (reverse)  | GACAGAAGTCTCGCATTCTTCC     | 117                   |


**Steps:**      
Notes: 
* I load 4 uL of cDNA into 6 uL of power sybr green master mix for 10 uL reactions   
* Samples are run in duplicates or triplicates  
* Starting out, I like to run my amplicons on agraose gels and sanger sequence them (another good line of evidence that you're detecting 1 product in addition to the the melt curve analysis at the end of the qpcr)        
* I use geneious version R6 (http://www.geneious.com/) to design primers and visualize sequences       

1) Prep cDNA: From previous step, you should have diluted 1/10. So you'll have 0.25 ng/uL now. I usually do this by adding 5 uL cDNA into 45 uL nuclease free water.    
2) Prep sybr green master mix: I add 250 nM of Forward and 250 nM of Reverse primer with power sybr green. 

| Reagent             | Inital conc. | Final conc. | uL for 1 rxn | 10 rxn set up |
| ------------------- | ------------ | ----------- | ------------ | ------------- |
| Power sybr green    | 2x           | 1x          | 5            | 50            |
| Forward Primer      | 10 uM        | 250 nM      | .25          | 2.5           |
| Reverse Primer      | 10 uM        | 250 nM      | .25          | 2.5           |
| nuclease free water | na           | na          | .5           | 5             |
| cDNA                | 0.25 ng/ul   | .1 ng/uL    | 4            | na            |
| Total               |              |             | 10           |               |

3) Load master mix into plate (6 uL)    
4) Load cDNA ( 4uL)    
5) place in ABI steponeplus for following rxn:     
* qpcr steps   
  1. 95 C, 10 minutes     
  2. 40 cycles of: 95 C for 15s, 60 C for 60 seconds and fluorescence acquisition,         

* Melt curve analysis    
  1. Reactions were heated to 95C 15 s    
  2. From 60 C, slowly heat up and measure fluoresence         

6) Save amplicon for sequencing
