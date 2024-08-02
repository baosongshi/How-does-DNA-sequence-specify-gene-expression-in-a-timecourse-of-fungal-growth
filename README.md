# How-does-DNA-sequence-specify-gene-expression-in-a-timecourse-of-fungal-growth
*******Introduction of the project*********

Given the output data contains gene expression counts for genes over 50 experiment samples,  and k-mer features, which describe a short sequence of nucleotides for each gene at the starting point, we program the codes to solve the following questions:

Firstly, make exploratory analysis to do a good description of data, and the results of this would be most helpful for the proceeding modeling. 
Secondly, find an appropriate generalised linear model for genes given design conditions. 
Thirdly, find a relatively small amount of motifs, which are useful to predict gene expression across design conditions. 

 


*******Packages required****************

Tidyr/tidyverse:   we use this R package to change the data format(for example,merge several columns to one column) for plotting and modeling.
ggplot2:  we use this R package to make a series of density plots, pca plot, clustering plot, residual diagnostic plot, confident level plot of coefficient estimates, fitted plot.
MASS:  we use this R package to build the negative binomial regression model through function “glm.nb”
glmmTMB/lme4:  we use this R package to try to fit a negative binomial mixed regression model
mpath:  we use the “glmregNB” function in this R package to fit a negative binomial model with lasso.



*********The main structure of each code files***************
Running Sequence:
( the codes are run in order, You can also see the  structure through title of each R chunk)

1.RNA_project_exploratory analysis.Rmd

1.1 Read data

1.2 Exploratory analysis: normalization and other data preprocessing steps

1.3 Exploratory analysis: series of density plots 
     
1.4 Exploratory analysis: PCA reduce dimension & clustering

1.5 Exploratory analysis:  Kruskal–Wallis test

1.6 Save data
   


2.RNA_project_modeling.Rmd


2.1 Data preprocess & define some evaluation functions

2.2 Negative binomial regression for one gene


2.3 Negative binomial regression for all genes

2.3.1 Human guided data preprocess

2.3.2  Negative binomial regression under 2,3,4,5 mers& stepwise results

2.3.3 Lasso shrinkage method

2.3.4 Model averaging
