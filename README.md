# GEMMA_preclinical
Omics integration of preclinical mouse data 
Design courtesy of Sylvie Rabot lab (sylvie.rabot@inrae.fr)
<img width="1151" height="725" alt="GEMMA_SYLVIE_STUDY_Design" src="https://github.com/user-attachments/assets/7148722e-fd89-45cb-8b6e-6af4bb186134" />

Pipeline - scripting done in R with the exception of XGBoost where it is ran in python
Feature selection
Each data type is processed by itself, beginning with QC and scaling (normalisation as needed). To reduce the dimensions and find most important features, 
Glmnet (https://glmnet.stanford.edu/articles/glmnet.html) and XGBoost (https://xgboost.readthedocs.io/en/stable/python/python_intro.html, python) are both performed; the top results based on importance score are selected. Logistic regression on FMT and ASD groups are performed. 

For multi-omics integration, MixOmics (https://mixomics.org/) and CorrPlot (with pvalue testing, https://cran.r-project.org/web/packages/corrplot/vignettes/corrplot-intro.html) are conducted.

MixOmics additional examples
 https://github.com/karoliinas/GEMMA_precilinical
 
Example results from GEMMA preclinical data

[sylvie_mixomics_circos2.pdf](https://github.com/user-attachments/files/22132260/sylvie_mixomics_circos2.pdf)


Please contact jake.lin@tuni.fi and sylvie.rabot@inrae.fr for additional questions
