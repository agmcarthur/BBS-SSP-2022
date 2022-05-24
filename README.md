# Bioinformatics session for Biochemistry and Biomedical Sciences Summer Scholars Program 2022 

![Scholars](/img/scholars.jpg)

Hosted by the [McArthur Lab](http://mcarthurbioinformatics.ca).

## Day 1: Thursday 2 pm - 4 pm

* Quick introductions & overview

### Introductory Talks (10-15 minutes each)

* Brian Alcock, Lead CARD Curator - Introduction Biocuration & CARD
* Amos Raphenya, Lead CARD Developer - Introduction of Software Engineering & RGI
* Arman Edalatmand, MSc Student - Natural Language Processing & AMR
* Andrew McArthur, Associate Professor - Antimicrobial Resistance & Outbreak Analysis

### Comprehensive Antibiotic Resistance Database

Introduction to the Comprehensive Antibiotic Resistance Database, focussing on the current public version, [card.mcmaster.ca](http://card.mcmaster.ca). At the heart of the CARD is the Antibiotic Resistance Ontology (ARO). After a brief demo, we will work through the following questions:

* Question #1. Browsing from the CARD home page, what are the seven major branches of the ARO?
* Question #2. How many major drug classes are represented in the ARO? Drill down to examine information for the antibiotic *fosfomycin*.
* Question #3. Using the search box, find the ARO term for the MCR-1.1 protein. Outline what drugs MCR-1.1 confers resistance to and via which mechanism. Explain the mechanism by exploring the ARO terms associated with MCR-1.1.
* Question #4. Contrast MCR-1.1 and [Mycobacterium tuberculosis embB mutant conferring resistance to ethambutol](https://card.mcmaster.ca/ontology/39910) genes. How does the mechanism of resistance differ between these two genes? What extra information is required in the embB detection model?
* Question #5. Using the Resistance Gene Identifier software, analyze plasmid HQ451074.1. Perfect = perfect matches to reference sequences in the CARD, Strict = allowable variants of the reference sequences in the CARD using curated cut-offs, Loose = sequences with similarity to CARD reference sequences, but outside of detection model cut-offs. Trying the RGI visualizations or the Chart View, which are all based on the ARO, and only using Perfect and Strict hits (keeping defaults: exclude nudge, high quality/coverage), what resistance genes or variants exist in this plasmid sequence, which drugs classes do they confer resistance to, and via which mechanisms?
* Question #6. Plasmid HQ451074.1 above confers resistance to the *nucleoside antibiotic* tunicamycin, but this is not explained by the Perfect and Strict hits. Can you explain this by looking at Loose hits? How good is the evidence?
* Question #7. Using the Resistance Gene Identifier software, analyze *Salmonella enterica* genome AE014613.1 (Perfect and Strict only). Which mutation-based antimicrobial resistance is present in this genome (*hint: sort by the SNP column*), i.e. which genes and effected drugs? Are any of these detected mutations from the same pathogen? Do you think this pathogen will be resistant to these drugs?

### *Salmonella* outbreak analysis

We are now going to analyze [45 *Salmonella enterica* genomes](/data/Salmonella_genomes) from an outbreak. These samples are from 2012, when Public Health Ontario encountered a spike in food poisoning from a number of locations in Ontario, later determined to be *Salmonella* by traditional culture methods. Each isolate had DNA extracted, sequenced, and genome assembled. 

These genomes have been run through the PARSNP algorithm to catalog whole-genome SNPs (less SNP dense regions indicative of horizontal gene transfer) and these SNPs were used to generate a [phylogenetic tree](/data/Salmonella_tree). You can view the tree using [TreeView](http://etetoolkit.org/treeview/).

* Question #11. Given that the reference sequence NC_011294 may be very closely related to the Ontario strains but all other reference sequences are from different MLSTs and outbreaks, is there any evidence that the Ontario samples do not reflect a single source outbreak of *Salmonella*? Think carefully about the bootstrap values.
* Question #12. Sample 17 is a Nurse suspected of poor hand hygiene leading to infection of a number of patients (sample 14, 11, 35), including himself. Does the RAxML tree provide evidence supporting this suspicion? Is there evidence of further hospital acquired infections?
* Question #13. Chicken burgers distributed by a local food supplier have been found to be contaminated with *Salmonella* (samples 4 & 5). Subsequently, several patients (samples 2, 7, 8, 15) known to have eaten (and possibly undercooked) these chicken burgers were additionally found to have *Salmonella* infections. Is there evidence of a single source of all these infections? Could the illness of additional patients possibly be explained by contaminated chicken burgers?

Unexpectedly, a single patient has proven abnormally resistant to antibiotics, suggesting the *Salmonella* is not the only pathogen involved, even though it is the only pathogen successfully isolated by culture. This patient has had their fecal [metagenome](/data/Salmonella_metagenome) sequenced and assembled by the McArthur lab. Use the Resistance Gene Identifier (part of http://card.mcmaster.ca) to screen these putative AMR alleles for antimicrobial resistance genes. Note: the predicted alleles may only be fragments, so use RGI's Low Quality/Coverage setting but still only look for Perfect/Strict hits.

* Question #14. For the single patient that is abnormally resistant to antibiotics, does the metagenomics analysis concur that resistance to drugs beyond trimethoprim or fluoroquinolones exists in this microbiome? Which additional drug classes may not work against this microbiome?
* Question #15. Clinical treatment of this patient illustrated failure of macrolide antibiotics. What AMR genes are possibly causing this resistance and what is the mechanism? Can you make a prediction of which pathogen beyond *Salmonella* could be infecting this patient?

## Day 2: Friday 10 am - 12 pm

### Introductory Talks  (10-15 minutes each)

* Keaton Smith, Co-Op Student - CARD*Shark & Biocuration
* Karyn Mukiri, MSc Student - Total Resistome Prediction
* Jalees Nasir, PhD Student - Genomic Surveillance of Viruses
* Andrew McArthur, Associate Professor - DNA Sequencing Technologies

### Monkeypox Lab


