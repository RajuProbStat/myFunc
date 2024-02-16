Supplementary information / reproducible research files for the manuscript
Title: "Bootstrap Tests for Simultaneously Monotone Ordering of Effects in a Two-Way ANOVA"

Authors: Raju Dey, Anjana Mondal and Somesh Kumar
In case of questions or comments please contact rajudey.cob1997@gmail.com; mondal.anjana25@gmail.com;
smsh@maths.iitkgp.ac.in

In order to reproduce all the Results, Tables and Figures presented in the manuscript and its 
Supplementary material we have made a folder "code" having the subfolders "code_functions",
"code_intermediate_results", "intermediate_results", "reproduce_results", and the files 
"README" and "master_script.R".
    
The sub folder "code_functions" contains the R scripts and each script contains two functions, 
one function is for the test statistic Q_1 and the other one is for the test statistics Q_2 and 
Q_3.

The sub folder "intermediate_results" contains ".RData" files of the intermediate results
of the simulation and the subfolder "code_intermediate_results" contains the R scripts for 
producing these ".RData" files.
    
The subfolder "reproduce_results" contains the files: "reproduce_results_code.R",
"reproduce_results.Rmd" and "reproduce_results.pdf". The R script "reproduce_results_code.R" 
takes the ".RData" files from the sub folder "intermediate_results" and creates the results, 
tables and figures presented in the manuscript as well as in the Supplementary Material of the 
manuscript.
    
To demonstrate the reproduced results, the files "reproduce_results.Rmd" and 
"reproduce_results.pdf" have been made in Rmarkdown.
    
First save the folder "code" and set the working directory of the RStudio to the that folder 
and then run the R script "reproduce_results_code.R". The R script "reproduce_results_code.R"
takes the .RData files from the sub folder "intermediate_results" and creates the results, 
tables and figures presented in the manuscript as well as in the Supplementary Material of 
the manuscript.

Since computation of the whole simulation can take several hours, intermediate results of the
simulation are saved as ".RData" files into the folder "intermediate_results". For faster 
computation, reduce the number of replicates, say, rep=500. The R scripts for creating the 
.RData files are performed in parallel on 16 cores on a linux server, but should also work 
under windows. If the machine used for computation is not able to compute on 16 cores 
simultaneously, the number of cores used for simulation should be reduced by changing the code
line "cl<-makeCluster(16)" in the R scripts.
    
    
For creating .RData files:

Create a folder "intermediate_results" and set the working directory of the RStudio 
to this folder.For reproducing the .RData files, run the R script "master_script.R".
The .RData files will be saved into the folder "intermediate_results".
    
  
    "Table3_a3_b2.RData" has been used to reproduce the part a=3, b=2 of the Table 3.

    "Table3_a3_b3.RData" has been used to reproduce the part a=3, b=3 of the Table 3.

    "Table3_a3_b4.RData" has been used to reproduce the part a=3, b=4 of the Table 3.

     
    "figure2_subplot1.RData" has been used to reproduce subplot 1 of Figure 2; 
    "figure2_subplot2.RData" has been used to reproduce subplot 2 of Figure 2;
    "figure2_subplot3.RData" has been used to reproduce subplot 3 of Figure 2; 
    "figure2_subplot4.RData" has been used to reproduce subplot 4 of Figure 2.

    "figure3_subplot1.RData" has been used to reproduce subplot 1 of Figure 3; 
    "figure3_subplot2.RData" has been used to reproduce subplot 2 of Figure 3;
    "figure3_subplot3.RData" has been used to reproduce subplot 3 of Figure 3; 
    "figure3_subplot4.RData" has been used to reproduce subplot 4 of Figure 3.

    "figure4_subplot1.RData" has been used to reproduce subplot 1 of Figure 4; 
    "figure4_subplot2.RData" has been used to reproduce subplot 2 of Figure 4;
    "figure4_subplot3.RData" has been used to reproduce subplot 3 of Figure 4; 
    "figure4_subplot4.RData" has been used to reproduce subplot 4 of Figure 4.

    "figure5_subplot1.RData" has been used to reproduce subplot 1 of Figure 5; 
    "figure5_subplot2.RData" has been used to reproduce subplot 2 of Figure 5;
    "figure5_subplot3.RData" has been used to reproduce subplot 3 of Figure 5; 
    "figure5_subplot4.RData" has been used to reproduce subplot 4 of Figure 5.

    "figure6_subplot1.RData" has been used to reproduce subplot 1 of Figure 6; 
    "figure6_subplot2.RData" has been used to reproduce subplot 2 of Figure 6.
    
    
    "supplement_figure1_subplot1.RData" has been used to reproduce 
     subplot1 of Figure 1 of the Supplementary Material; 

    "supplement_figure1_subplot2.RData" has been used to reproduce
     subplot2 of Figure 1 of the Supplementary Material;

    "supplement_figure1_subplot3.RData" has been used to reproduce
     subplot3 of Figure 1 of the Supplementary Material;

    "supplement_figure1_subplot4.RData" has been used to reproduce
     subplot4 of Figure 2 of the Supplementary Material;

    "supplement_figure2_subplot1.RData" has been used to reproduce 
     subplot1 of Figure 2 of the Supplementary Material; 

    "supplement_figure2_subplot2.RData" has been used to reproduce 
     subplot2 of Figure 2 of the Supplementary Material;

    "supplement_figure2_subplot3.RData" has been used to reproduce
     subplot3 of Figure 2 of the Supplementary Material;

    "supplement_figure2_subplot4.RData" has been used to reproduce
     subplot4 of Figure 2 of the Supplementary Material;

    "supplement_figure3.RData" has been used to reproduce 
     Figure 3 of the Supplementary Material;

    "supplement_figure4.RData" has been used to reproduce
     Figure 4 of the Supplementary Material.



