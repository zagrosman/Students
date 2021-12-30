# This is a tutorial for quality control of fastq.gz files of NGS outputs by H. Rasouli
> December 23, 2021   ( ͡👁️ ͜ʖ ͡👁️)

![image](https://user-images.githubusercontent.com/17006122/146686434-cd019170-e7d2-459e-a2b8-3a6edacf6383.png)

# Installation procedure.

To get the binary files of FastqCleaner you can use this URL: https://github.com/leandroroser/FastqCleaner
Original tutorial can be obtained from this link: https://leandroroser.github.io/FastqCleaner/articles/Overview.html

# Issues with installation and launching FastqCleaner:

There was a problem with the installation of fastqcleaner that I informed the developer team and now it was solved. To install this tool you can follow the below procedures
1. To run the software, you will need to install both R and RStudio. Next, open the RStudio and install the following packages:

a. Devtools
````````
install.packages("devtools")
````````
b. Load devtools library:
````````
library(devtools)
````````
c. Install the fastqCleaner:
````````
devtools::install_github("https://github.com/leandroroser/FastqCleaner")
````````
d. Load fastqcleaner library and launch the software:
````````
library('FastqCleaner')
launch_fqc()
````````

2. A webpage like the below figure will be showed on your web-browser:
![image](https://user-images.githubusercontent.com/17006122/146686697-01177599-e520-4726-a2c7-359c2aa1c0db.png)

Now you can use it and try to do quality control of your sequenced reads



# Please use the following file to run FastqCleaner:

https://uupload.ir/view/example_11ur.zip/

