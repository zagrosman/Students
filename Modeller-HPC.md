
![image](https://user-images.githubusercontent.com/17006122/156988502-8ae62f83-2885-46d6-a420-d6e04fe3c6d4.png)

## This is a tutorial to install modeller software on your HPC system. 
*****************************************************************
MODELLER is used for homology or comparative modeling of protein three-dimensional structures (1,2).
The user provides an alignment of a sequence to be modeled with known related structures and MODELLER automatically calculates a model containing all non-hydrogen atoms.
MODELLER implements comparative protein structure modeling by satisfaction of spatial restraints (3,4), and can perform many additional tasks, including de novo modeling of loops in protein structures, optimization of various models of protein structure with respect to a flexibly defined objective function, multiple alignment of protein sequences and/or structures, clustering, searching of sequence databases, comparison of protein structures, etc.
**Link to modeller official website:**
https://salilab.org/modeller/


1. B. Webb, A. Sali. Comparative Protein Structure Modeling Using Modeller. Current Protocols in Bioinformatics 54, John Wiley & Sons, Inc., 5.6.1-5.6.37, 2016.
2. M.A. Marti-Renom, A. Stuart, A. Fiser, R. Sánchez, F. Melo, A. Sali. Comparative protein structure modeling of genes and genomes. Annu. Rev. Biophys. Biomol. Struct. 29, 291-325, 2000.
3. A. Sali & T.L. Blundell. Comparative protein modelling by satisfaction of spatial restraints. J. Mol. Biol. 234, 779-815, 1993.
4. A. Fiser, R.K. Do, & A. Sali. Modeling of loops in protein structures, Protein Science 9. 1753-1773, 2000.

*****************************************************************

## Installation steps:
1. Step 1: Check if you previously installed Modeller or not:

````
$ module avail modeller
````

2. Load Modeller if there was installed:

````
$ module load modeller/9.17
````

3. Install the modeller:

````
$ cd /tmp/
$ wget -qO - https://salilab.org/modeller/9.17/modeller-9.17.tar.gz | tar -zxv
$ cd modeller-9.17
$ sudo mkdir -p /export/apps/modeller/9.17/
$ sudo chown joguya:joguya /export/apps/modeller/9.17/
$ module load python/3.4.3
$ ./Install
$ sudo chown -R root:root /export/apps/modeller/9.17/
````

