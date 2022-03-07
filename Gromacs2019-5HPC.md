![image](https://user-images.githubusercontent.com/17006122/156988869-f6f5e426-efb7-468f-bbf0-e52662feb3d7.png)

## This is a simple installation guide to download and install Gromacs-2019.5 on HPC syestem.
********************************************************************************************
GROMACS is a molecular dynamics package mainly designed for simulations of proteins, lipids, and nucleic acids. 
It was originally developed in the Biophysical Chemistry department of University of Groningen, and is now maintained by contributors in universities and research centers worldwide.
There are some useful links you can use for installation and downloading the gromacs toolbox:

1. **Link to download page**: https://manual.gromacs.org/documentation/
2. **Link to documentation page**:https://manual.gromacs.org/current/user-guide/index.html
********************************************************************************************



## Installation procedure
To install gromacs 2019v5 on your HPC you can follow the belowing instructions. 

## download the gromacs
````
1) wget ftp://ftp.gromacs.org/pub/gromacs/gromacs-2019.5.tar.gz
````

## unzip its source
````
2) tar xfz gromacs-2019.5.tar.gz
````

## go to the folder 

````
3) cd gromacs-2019.5
````

## download the regressiontests locally
````
4) wget https://ftp.gromacs.org/regressiontests/regressiontests-2019.5.tar.gz

##unzip regressiontests files
5) tar xfz regressiontests-2019.5.tar.gz

##go to its path
6) cd regressiontests-2019.5

## save the path
7) pwd ## for example: /root/gromacs-2019.5/regressiontests/regressiontests-2019

8) cd ..

## create a folder in gromacs 

9) mkdir build

10) cd build
````
 

## modified cmake command: -DREGRESSIONTEST_PATH address should be set based on your local path of unzipped regressiontest
````
11) cmake .. -DGMX_GPU=OFF -DGMX_BUILD_OWN_FFTW=ON -DREGRESSIONTEST_DOWNLOAD=OFF -DREGRESSIONTEST_PATH=**/root/gromacs-2019.5/regressiontests/regressiontests-2019** -DGMX_MPI=on -DCMAKE_INSTALL_PREFIX=**/root/gromacs-2019.5**
 -DCMAKE_C_COMPILER=gcc -DCMAKE_CXX_COMPILER=g++

12) make

13) make check

14) sudo make install
````

## Please note that instead of this address we should add our path that gromacs will be installed into it something like: /root/gromacs-2019.5/build/bin/GMXRC
````
15) source /usr/local/gromacs/bin/GMXRC 
````

## Step 2 installation

After doing the above mentioned steps:
````
1) cd .. ## you should exit the build folder and back to gromacs folder
````
2) mkdir build-normal
````
3) cd build-normal
````
## For this step we should specify the path cmake install in previous section. only type the following command
````
4) cmake .. -DCMAKE_INSTALL_PREFIX= ##gromacs "bulid" (section 9 in step 1) foler path here something like "/root/gromacs-2019.5/build"
````
5) make -j 16
````
6) make install
````

## Step 3 installation

Again exit from build-normal path and try to create another directory

````
1) cd ..
````
````
2) mkdir build-mdrun-only
````
````
3) cd mkdir build-mdrun-only
````
````
4) cmake .. -DGMX_MPI=ON -DGMX_GPU=OFF -DGMX_BUILD_MDRUN_ONLY=ON -DCMAKE_INSTALL_PREFIX= **gromacs "bulid" (section 9 in step 1) foler path here something like "/root/gromacs-2019.5/build"**
````
````
5) make -j 16
````
````
6) cd ..
````
7) cd /to/your/unpacked/regressiontests-2019.5
````

````
8) source /your/installation/prefix/here/bin/GMXRC ### for this section you should add your build installation folder to path  something like /gromacs/build/bin/GMXRC
````

````
9) add the path to bashrc file and type "gmx" in terminal

````



