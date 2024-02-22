Supplementary information / reproducible research files for the manuscript
Title: "Bootstrap Tests for Simultaneous Monotone Ordering of Effects in a Two-Way ANOVA"

Authors: Raju Dey, Anjana Mondal and Somesh Kumar
In case of questions or comments please contact rajudey.cob1997@gmail.com; mondal.anjana25@gmail.com;
smsh@maths.iitkgp.ac.in

In order to reproduce all the results, tables and figures presented in the manuscript and its 
supplementary material, we have made a folder "code_results" having the subfolders "code_functions",
"code_intermediate_results", "intermediate_results", "reproduce_results", and the file "README". 

    
The sub folder "code_functions" contains six R scripts and each script contains two functions, 
the first function is for the test statistic Q_1 and the second one is for the test statistics 
Q_2 and Q_3. The six R scripts are
                      (i)   Q1_Q2_Q3_robust_skewed_a_3_b_3.R
                      (ii)  Q1_Q2_Q3_robust_symmetric_a_3_b_3.R
                      (iii) Q1_Q2_Q3_size_power_a_3_b_2.R
                      (iv)  Q1_Q2_Q3_size_power_a_3_b_3.R
                      (v)   Q1_Q2_Q3_size_power_a_3_b_4.R 
                      (vi)  real_data_functions.R

The functions inside the R script "Q1_Q2_Q3_robust_skewed_a_3_b_3.R" have been used to evaluate
the size and power values of the test statistics Q_1, Q_2 and Q_3 when the distributions of 
the random observations are skewed (Weibull, exponential, log-normal, chi-square, mixture-I, 
mixture-II) and a=3, b=3.

The functions inside the R script "Q1_Q2_Q3_robust_symmetric_a_3_b_3.R" have been used to 
evaluate the size and power values of the test statistics Q_1, Q_2 and Q_3 when the 
distributions of the random observations are non-normal symmetric (t_5, Laplace, Cont. Normal,
Uniform) and a=3, b=3.

The functions inside the R script "Q1_Q2_Q3_size_power_a_3_b_2.R" have been used to evaluate
the size and power values of the test statistics Q_1, Q_2 and Q_3 when the distributions of 
the random observations are normal and a=3, b=2.

The functions inside the R script "Q1_Q2_Q3_size_power_a_3_b_3.R" have been used to evaluate
the size and power values of the test statistics Q_1, Q_2 and Q_3 when the distributions of
the random observations are normal and a=3, b=3. 

The functions inside the R script "Q1_Q2_Q3_size_power_a_3_b_4.R" have been used to evaluate
the size and power values of the test statistics Q_1, Q_2 and Q_3 when the distributions of
the random observations are normal and a=3, b=4. 

The functions inside the R script "real_data_functions.R" have been used to find the observed 
test statistic values and the critical values of the test staistics Q_1, Q_2 and Q_3 for a
given data set. 


The sub folder "intermediate_results" contains ".RData" files of the intermediate results
of the simulation and the subfolder "code_intermediate_results" contains the R scripts 
("results_figures.R", "results_supplementary_figures.R" and "results_tables.R") which have 
been used to produce these ".RData" files.

    
The subfolder "reproduce_results" contains the files: "master_script_results_analyses.R",
and "reproduce_results.pdf".  The R script "master_script_results_analyses.R" 
(code lines "8-234") produce all the ".RData" files saved as the intermediate results. 
The R script "master_script_results_analyses.R" (code lines "247-1189") takes the 
".RData" files from the sub folder "intermediate_results" and creates all the results, 
tables and figures presented in the manuscript and its supplementary material. 
To demonstrate the reproduced results for the manuscript as well its supplementary material,
"reproduce_results.pdf" have been made in Rmarkdown.
    

For reproducing the ".RData" files:
Create a folder "intermediate_results" and set the working directory of the RStudio 
to this folder. Then run the code lines "8-234" from the 
R script "master_script_results_analyses.R". The ".RData" files will be saved into the folder 
"intermediate_results".


For reproducing all the results, tables and figures of the manuscript and its supplementary
material using .RData files: First save the folder "code_results" and set the working 
directory of the RStudio to that folder and then run the code lines "247-1189" from the R 
script "master_script_results_analyses.R". Taking the ".RData" files from the sub folder 
"intermediate_results", it creates all the results, tables and figures presented in the 
manuscript as well as in the supplementary material of the manuscript.


Since computation of the whole simulation can take several hours, intermediate results 
of the simulation are saved as ".RData" files into the folder "intermediate_results". For 
faster computation, reduce the number of replicates, say, rep=500 (from the R scripts 
belong the sub folder "code_intermediate_results"). The R scripts for creating these
".RData" files are performed in parallel on 16 cores on a Linux server, but should also work 
under Windows. If the machine used for computation is not able to compute on 16 cores 
simultaneously, the number of cores used for simulation should be reduced by changing the 
code line "cl<-makeCluster(16)" in the R scripts (i)-(vi).
    

    
The code is written in R with the following software versions:
R version 4.2.3 (2023-03-15 ucrt)
Platform: x86_64-w64-mingw32/x64 (64-bit)

Matrix products: default

locale:
 [1] LC_COLLATE=English_India.utf8  LC_CTYPE=English_India.utf8
 [3] LC_MONETARY=English_India.utf8 LC_NUMERIC=C
 [5] LC_TIME=English_India.utf8

attached base packages:
 [1] parallel stats    graphics   grDevices utils   datasets  methods
 [8] base

other attached packages:
 [1] latex2exp_0.9.6  doParallel_1.0.17 iterators_1.0.14  foreach_1.5.2
 [5] matlib_0.9.6     Iso_0.0-21        kableExtra_1.3.4  knitr_1.45

loaded via a namespace (and not attached):
  [1] compiler_4.2.3    base64enc_0.1-3   tools_4.2.3       digest_0.6.31
  [5] jsonlite_1.8.4    evaluate_0.23     lifecycle_1.0.4   viridisLite_0.4.2
  [9] rlang_1.1.0       cli_3.6.1         rstudioapi_0.15.0 yaml_2.3.7
 [13] xfun_0.40         fastmap_1.1.1     httr_1.4.6        stringr_1.5.1
 [17] xml2_1.3.5        htmlwidgets_1.6.4 systemfonts_1.0.4 webshot_0.5.5
 [21] svglite_2.1.3     glue_1.6.2        R6_2.5.1          rgl_1.2.1
 [25] rmarkdown_2.25    carData_3.0-5     car_3.1-2         magrittr_2.0.3
 [29] codetools_0.2-19  scales_1.3.0      htmltools_0.5.7   MASS_7.3-59
 [33] abind_1.4-5       rvest_1.0.3       colorspace_2.1-0  xtable_1.8-4
 [37] stringi_1.7.12    munsell_0.5.0

Simulations (for creating the ".RData" files) are run on in parallel on a Linex server 
with the software versions:
R version 4.1.2 (2021-11-01)
Platform: x86_64-pc-linux-gnu (64-bit)
Running under: Ubuntu 22.04.3 LTS

Matrix products: default
BLAS: /usr/lib/x86_64-linux-gnu/blas/libblas.so.3.10.0
LAPACK: /usr/lib/x86_64-linux-gnu/lapack/liblapack.so.3.10.0

locale:
  [1] LC_CTYPE=en_IN.UTF-8       LC_NUMERIC=C
  [3] LC_TIME=en_IN.UTF-8        LC_COLLATE=en_IN.UTF-8
  [5] LC_MONETARY=en_IN.UTF-8    LC_MESSAGES=en_IN.UTF-8
  [7] LC_PAPER=en_IN.UTF-8       LC_NAME=C
  [9] LC_ADDRESS=C               LC_TELEPHONE=C
 [11] LC_MEASUREMENT=en_IN.UTF-8 LC_IDENTIFICATION=C

attached base packages:
 [1] parallel  stats    graphics  grDevices utils     datasets  methods
 [8] base

other attached packages:
 [1] latex2exp_0.9.6   doParallel_1.0.17 iterators_1.0.14  foreach_1.5.2
 [5] Iso_0.0-21

loaded via a namespace (and not attached):
  [1] codetools_0.2-18 digest_0.6.33    lifecycle_1.0.4   magrittr_2.0.3
  [5] evaluate_0.23    rlang_1.1.2      stringi_1.8.3     cli_3.6.2
  [9] vctrs_0.6.5      rmarkdown_2.25   tools_4.1.2       stringr_1.5.1
 [13] glue_1.6.2       yaml_2.3.8       xfun_0.41         fastmap_1.1.1
 [17] compiler_4.1.2   htmltools_0.5.7  knitr_1.45











