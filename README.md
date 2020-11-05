# lavfit  
Calculate Construct Reliability (CR) and the Average Variance Extracted (AVE) in Lavaan structural models.   
  
##Installation  
This package require the lavaan library (structural equation modeling).  
Download the lavfit.tar.gz file.  
In Rstudio, click on the Packages tabs, install and choose install from Package Archive.  

##Usage  
After the lavaan estimation  
estim = sem(model,data)  
or estim = cfa(model,data)  
  
insert this code  
lavfit(estim)  

##Example :   
library(lavaan)  
library(lavfit)  
  
model <- '  
A =~ A1 + A2 + A3  
B =~ B1 + B2 + B3  
'  
estim <- sem(model,data)  
summary (estim)  
  
lavfit(estim)  
  
Results :  
      CR   AVE  
A   0.857 0.602  
B   0.894 0.679  
