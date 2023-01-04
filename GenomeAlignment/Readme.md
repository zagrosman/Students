## Vista-based genome alignments
VISTA is an application that allows the visualization of long 
sequence alignments with annotation information.

The VISTA program uses the file or files (to visualize several 
related alignments) produced by any procedure of global or 
local alignment (such as BLAST, Gap (GCG), etc.) of two 
DNA sequences and parsed by the user according to 'Alignment_file' 
format (see Appendix I).

The VISTA plot is based on moving a user-specified window over 
the entire alignment and calculating the percent identity over 
the window at each base pair. The X-axis represents the base 
sequence; the Y-axis represents the percent identity. If the user 
supplies an annotation file (see Appendix II), genes and exons 
are marked above the plot. The direction of genes is indicated by 
an arrow, while the coding exons and UTRs are marked with 
rectangles of different color. Conserved regions are highlighted 
under the curve, with red indicating a conserved non-coding region 
and blue indicating a conserved exon. Conserved UTRs are colored 
turquoise. The colors can be modified by the user. 

A conserved region is defined with percentage and length 
cutoffs. Conserved segments with percent identity X and 
length Y are defined to be regions in which every contiguous 
subsegment of length Y was at least X% identical to its 
paired sequence. These segments are merged to define 
the conserved regions. 

VISTA can be configured (see Appendix III) for visualizing 
alignments of various lengths by changing several parameters: 
the number of pages on which the output appears, the number of 
frames per page, the window size, and the resolution at which 
the alignment is plotted. VISTA allows one to easily create 
figures for various documents. For simplicity it is also 
possible to specify only a subset of these parameters, with 
the rest being automatically calculated. VISTA also supports 
simultaneous visualization of several related alignments. 

Installation:

Create a directory and copy Vista.jar and retepPDF2.jar to it. 
Then change your CLASSPATH environment variable to include 
references to these two files.

Example I (Windows):

1. mkdir c:\vista
2. copy source_path\Vista.jar c:\vista
3. copy source_path\retepPDF2.jar c:\vista
4. set CLASSPATH=c:\vista\Vista.jar;c:\vista\retepPDF2.jar

Example II (UNIX, csh/tcsh):

1. mkdir target_path/vista
2. cp source_path/Vista.jar target_path/vista
3. cp source_path/retepPDF2.jar target_path/vista
4. setenv CLASSPATH "target_path/vista/Vista.jar:target_path/vista/retepPDF2.jar"

Example III (UNIX, sh/bash):

1. mkdir target_path/vista
2. cp source_path/Vista.jar target_path/vista
3. cp source_path/retepPDF2.jar target_path/vista
4. export CLASSPATH="target_path/vista/Vista.jar:target_path/vista/retepPDF2.jar"

Usage: java Vista [-options] plot_file

 where "plot_file" is the name of a file containing plot 
 parameters (for file format see Appendix III),
 and options include:
   -q   turn on quiet mode
   -d   turn on debug mode

Dependencies:

1) needs a JVM 1.2.1 or better available from http://java.sun.com/

2) requires the uk.org.retepPDF library available from
   http://www.retep.org.uk/pdf/. A copy of the library and 
   its source code with our bug fixes are provided with VISTA.

----------
You can find additional details on VISTA at http://www-gsd.lbl.gov/vista.
Please email vista@lbl.gov with your questions, comments and suggestions.

----------
Appendix I
----------

Note:
We are working on a parser to convert BLAST alignment output format 
to VISTA format.

Alignment_file format:

Column 1 - ordinal numbers of the nucleotides in the first sequence
Column 2 - first sequences
Column 3 - '-' if there is an exact nucleotide match in the alignment, 
           and ' ' (space) if there is no match.
Column 4 - aligned nucleotide of the second sequence, or '|' for 
           the insertion.
Column 5 - ordinal numbers of the nucleotides in the second sequence.

Sample alignment file:

1   c   |
2   t   |
3   g   |
4   a - a  1
5   c   |
6   t   |
7   a - a  2
8   g   |
9   g   |
10  a - a  3
11  g   |
12  g   |
13  g   |
14  c   |
15  t - t  4
16  g   c  5
17  a - a  6
18  t   |
19  t   |
20  t   |
21  g - g  7
22  t - t  8
23  a   |
24  a - a  9
25  g - g  10
26  t   |
27  t   |
28  g - g  11
29  g - g  12
30  t   |
31  a   |
32  a - a  13
33  g - g  14
34  a - a  15
35  c   |
36  t   g  16
37  g - g  17
38  t   a  18
39  a - a  19
40  g - g  20
41  c   |

-----------
Appendix II
-----------

Annotation_file format: 

The start and the finish for each gene, as well as the name 
should be listed on one line. A greater than or less than sign 
should be placed before this line to indicate plus strand >, 
or minus strand <, although the numbering should be according 
to the plus strand. The exons should then be listed individually 
with the word exon after the start and finish of each exon. UTRs 
are annotated the same way an exon is, with the word utr 
replacing exon. 

For example: 

< 106481 116661 unknown 
106481 106497 utr 
107983 108069 exon 
109884 110033 exon 
111865 112023 exon 
114352 114562 exon 
116587 116661 utr 
> 39424 42368 GDF 9 
39424 39820 exon 
41401 42368 exon 

------------
Appendix III
------------

Plotfile format (all parameter names are case-insensitive):

TITLE title_name
  Specifies the title of the plot, printed in the legend.
  Defaults to nothing.
  Optional.

OUTPUT filename
  Specifies the pdf file to write to.
  Defaults to testpage.pdf
  If filename extension is ".jpg" or ".jpeg", plot will be saved 
  in JPEG format.
  Optional.

ALIGN align_file in_format
  SEQUENCES human mouse
  REGIONS min_id min_length
  MIN pltMin
  DIFFS ON | OFF | AUTO | max_percent
  PLOT ON | OFF
  REGION_FILE reg_file
  SCORE_FILE score_file
  ALIGNMENT_FILE align_file out_format
  CONTIGS_FILE contigs_file
  USE_ORDER ON | OFF
END
  Specifies the parameters for a pair-wise alignment to be plotted. 
  If you have two or more alignments, you have to include an  
  "ALIGN" section for each of them in the plotfile. If you have 
  a multiple alignment, you have to split it into pair-wise 
  components and include an "ALIGN" section for each of them in 
  the plotfile.

  "align_file" is the file containing the alignment; required.

  "in_format" is the format of the alignment: GLASS or BINARY;
  defaults to GLASS if omitted.

  "min_id" is the %id criteria to color regions; defaults to 70.

  "min_length" is the min region size to color; defaults to 100.

  "pltMin" is the bottom of the plotting scale; defaults to 50.

  If DIFFS is specified the Y-axis of the plot will represent 
  the percent difference instead of the percent identity;
  "max_percent" is the top of the plotting scale;
  AUTO parameter allows to choose automatically between plotting 
  difference or identity depending on how close the organisms are;
  optional; defaults to OFF.

  If "PLOT OFF" is specified VISTA will not make the plot; optional;
  defaults to ON.
  
  REGION_FILE is the file to save the regions in; optional.

  SCORE_FILE is the file to save the scores in; optional.

  ALIGNMENT_FILE is the file to save the alignment in; optional.
  "out_format" is the format of the saved alignment: GLASS, BINARY 
  or BLAST; defaults to BLAST if omitted.

  CONTIGS_FILE is the file that contains the list of contigs in
  the merged sequence for the second species; optional.

  If "USE_ORDER ON" is specified, VISTA will use the order in which the contigs
  go in the CONTIGS_FILE for numbering them in the picture; optional;
  defaults to OFF.

GENES annotation_file format
  Specifies the file to read the gene & exon annotation from.
  "annotation_file" is the file to read; required.
  "format" is the format of the file: GFF or SIMPLE; defaults 
  to SIMPLE if omitted (for the format details see README).
  Optional.

COORDINATE sequence
  Specifies which sequence to use as the coordinate.
  "sequence" must be one of the sequences specified with 
  the SEQUENCE parameter in an ALIGN section.
  Required.

START base_num
  Specifies the coordinate base number to start plotting at.
  "base_num" must be [1,N] where N is the number of bases
  in the coordinate sequence.
  Defaults to 1.

END base_num
  Specifies the coordinate base number to start plotting at.
  "base_num" must be [1,N] where N is the number of bases
  in the coordinate sequence.
  Defaults to N.

PAPER paper_type
  Specifies the paper format to use. 
  "paper_type" must be either letter or A4.
  Defaults to letter if omitted.

NUM_PAGES n
  Specifies the number of pages the plot should be.  If this 
  is used the BASES parameter will be automatically calculated.
  If omitted:
    1) gets automatically calculated if BASES is specified;
    2) otherwise defaults to 1.

BASES num_bases
  Specifies the number of bases to be plotted on each line.
  Gets automatically calculated if omitted or if NUM_PAGES 
  is specified.

TICK_DIST distance
  "distance" is the number of bases between number markers 
  on the X axis.
  Defaults to 10 ticks one each line if omitted.

RESOLUTION n
  Specifies how often to plot a score.
  If omitted it is set to the best resolution available - one 
  score per pixel.

WINDOW winSize
  Specifies the window size from which scores are calculated.
  If omitted or invalid it is set to the min region size used 
  to color regions from the first specified alignment.

NUM_WINDOWS n
  Obsolete.

NUM_PLOT_LINES n
  Specifies how many lines of the plot to put on a page.
  If omitted:
    1) gets automatically calculated if BASES is specified and
       NUM_PAGES is omitted (maximum value is 4);
    2) otherwise defaults to 4.

LEGEND ON | OFF
  If ON is specified a legend is printed on the left side 
  of the plot.
  Optional.
  Defaults to OFF.

FILENAME ON | OFF
  If ON is specified the legend will print the filename
  for each alignment. Otherwise the alignment number is printed.
  Optional.
  Defaults to OFF.

COLOR region_type R G B
  Specifies the color used to color a particular region. 
  "region_type" should be one of EXON, CNS (conserved, non-coding), 
  or UTR.  R, G, & B are integers [0,255] specifying the intensity 
  of the given color component.
  Optional.

AXIS_LABEL where
  Turns on labeling of the Y axis. "where" is either TOP, MIDDLE, 
  BOTTOM, or ALL. If "where" is omitted the ALL option is assumed.
  Optional.

TICKS_FILE filename
  If this option is specified the program will put colored tick 
  marks on the center line of the plot. The "filename" contains 
  the regions and colors of the ticks. Each line of the file 
  is as follows:
  START END COLOR
  where START is the beginning of the region, END is the end of 
  the region and COLOR is the color of the tick (a number 
  from 1 to 12; 1 - green, 2 - magenta, 3 - orange, 4 - yellow, 
  5 - red, 6 - dark orange, 7 - blue, 8 - light green, 
  9 - light blue, 10 - fern green, 11 - purple, 12 - brick). 
  The tick position is equal to (START + END) / 2.
  Optional.

GAPS ON | OFF | min_gap
  "min_gap" specifies the minimum gap that will be shown 
  on the plot; defaults to 100 if ON is specified.
  If OFF is specified, no gaps will be shown.
  Optional.
  Defaults to OFF.

SNPS_FILE filename
  If this option is specified the program will draw SNPs 
  positions above the plot. The "filename" contains the 
  positions of SNPs (one position per line).
  Optional.

REPEATS_FILE filename
  If this option is specified the program will draw repeats 
  above the plot. The "filename" contains repeats found by RepeatMasker.
  Optional.

FILTER_REPEATS ON | OFF
  If ON is specified repetitive elements will be filtered out from 
  the conserved regions.
  Optional.
  Defaults to OFF.

I/U window start_1 end_1 step_1 start_2 end_2 step_2 start_3 end_3 step_3
  If this option is specified the program will use I/U analyses
  to determine percent identity cutoffs to define actively conserved
  noncoding sequences in the first three alignments.
  "window" is the length cutoff for CNSs; defaults to 100.
  For each alignment "start_n", "end_n" and "step_n" define the range 
  of percent identity cutoffs for which I/U analyses are performed; 
  default to 70, 100 and 1 respectively.
  Optional.
