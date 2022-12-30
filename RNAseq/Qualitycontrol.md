
## RNAseq reads quality control

To set off your first RNAseq project, you can follow the below steps to start RNAseq analyses. 

1. Using following commands make a working directory in target path. First, I start with QC step:

**Make a working folder**

1. ``` $ mkdir project```
2. ``` $ cd project```
3. ``` $ mkdir QC```



cd $RNA_HOME/student_tools/
wget https://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.8.zip --no-check-certificate
unzip fastqc_v0.11.8.zip
cd FastQC/
chmod 755 fastqc
./fastqc --help
