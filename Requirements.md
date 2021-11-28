---
title: "Analyses of genome data"
author: "Maria Izabel Cavassim Alves"
date: "11/24/2021"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

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
