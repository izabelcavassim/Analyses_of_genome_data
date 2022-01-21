---
title: "Analyses of genome data - QCBio Collaboratory"
author: "Maria Izabel Cavassim Alves"
date: "11/24/2021"
output: html_document
---
Workshop description
=====================

High-throughput sequencing technologies have allowed researchers to extract DNA at the individual, population, and species levels. 
In this workshop, students will learn how to analyze and interpret population-level genetic information with PLINK and R.
Students will also be exposed to the literature on the different topics, followed by hands-on exercises and paper discussion.


Learning goals
=====================
At the end of this workshop, the students will be able to:

* Describe what a variant calling file (VCF) format is and how to manage those files.
* Conduct quality assesment of a VCF.
* Learn about population structure and how to compute it with PLINK.
* Learn about linkage disequilibrium and how to compute it with PLINK.
* Learn about basic association testing and genome wide association studies (GWAS).
* Learn about copy number variants (CNVs) and how to test for common CNVs across indidviduals.
* Discuss original literature within the subjects.


Day 1 (3 hours)
=====================
* Background lecture (45 minutes)
	- What is a VCF?
	- What is QC, and why is it so important?
* Break (15 minutes)
* Hands on exercise (1 hour)
	- VCF Data management (read, recode, reorder, merge, subset, compress data)
	- QC assessement
* Break (15 minutes)
* Paper discussion on quality control assessment (30 minutes)
* Assignment explanation (15 minutes)


Day 2 (3 hours)
=====================
* Background lecture (45 minutes)
	- What is population structure?
	- What is linkage disequilibrium?
	- How does population structure and LD affect association mapping?
* Break (15 minutes)
* Hands on exercise (1 hour)
	- Population stratification detection
	- LD estimation
* Break (15 minutes)
* Paper discussion on genome wide association studies
* Assignment explanation (15 minutes)


Day 3 (3 hours)
=====================
* Peer review of previous assignment (15 minutes)
* Background lecture (45 minutes)
	- What is association testing and GWAS?
	- What is a Manhattan plot and a Q-Q plot?
	- What is a copy number variant?
* Break (15 minutes)
* Hands-on exercise (1 hour and 30 minutes)
	- Basic association testing
	- GWAS accounting for population structure
	- CNV detection
* Break (15 minutes)
* Assignment explanation (15 minutes)

Helpful links if you get stuck during this exercise:

* [PLINK2 documentation](https://www.cog-genomics.org/plink2/)
* [Introduction to the linux command line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-commandline-for-almost-anything)


# Accessing hoffman2
If you have a macbook or linux, you can open the terminal and type the following:
```{bash, eval=F}
ssh [YOUR_LOGIN_NAME]@hoffman2.idre.ucla.edu
```
It will request your password and once you type it you are in!Yay!

If you have a windows machine, then I would recommend you following the instructions provided in the hoffman2 [website](https://www.hoffman2.idre.ucla.edu/Using-H2/Connecting/Connecting.html).

# To Install R
Open an internet browser and go to www.r-project.org.
Click the "download R" link in the middle of the page under "Getting Started."
Select a CRAN location (a mirror site) and click the corresponding link.
Click on the "Download R for (Mac) OS X" link at the top of the page.
Click on the file containing the latest version of R under "Files."
Save the .pkg file, double-click it to open, and follow the installation instructions.
Now that R is installed, you need to download and install RStudio.

# To Install RStudio
Go to www.rstudio.com and click on the "Download RStudio" button.
Click on "Download RStudio Desktop."
Click on the version recommended for your system, or the latest Mac version, save the .dmg file on your computer, double-click it to open, and then drag and drop it to your applications folder.

Once we are all able to access the cluster we can then install [PLINK](https://www.cog-genomics.org/plink2/)!

First download the file from their [website](https://www.cog-genomics.org/plink2/): 
then go to the terminal in your computer and go to where your file is via *cd*, mine is in the Downloads folder, so I can type:

```{bash, eval=F}
cd Downloads
scp plink_linux_x86_64_20210606.zip mica20@hoffman2.idre.ucla.edu:/u/home/m/mica20/project-collaboratory/PLINK_exercises/
```

Now go to the open window you have that gives you access to the cluster and unzip the file in the cluster by typing:

```{bash, eval=F}
unzip plink_linux_x86_64_20210606.zip
```

Now you are ready to use plink, type the following to see if works
```{bash, eval=F}
./plink
```
