# HACKATON: *LHC ALERT LEVELS DETECTION*
Hackaton Kaggle competition of Statistical Learning course, University La Sapienza, Rome (IT).\
The competitons lasted 48 hours and saw 15 teams of students from Scienze Statistiche, Data Science and Statistical Methods for Data science degree courses compete against each other.

![ECF16231-D400-4131-A5D7-90D10F92F9A9-1024x614](https://github.com/giuseppedipoce/HACKATON-LHC-alert-detection/assets/114066138/5172a233-c443-4b9e-aef2-a226e3c55276)



## Brief description of the task

Briefly speaking the task assigned during this hackathon was to correctly classify three alert levels 
(target variable) in the high-frequency work of compressors located inside the particle accelerator (LHC) at CERN,Geneva.
The dataset shows a very strong imbalance in the target
alert level 3, which is the most important (and difficult) to classify.
The data are presented in the form of time series, informed by 
time period of detection of the compressors and the location
in which it is located within the accelerator.


## Features extraction and model selection

Our team developed, in the light of the data handled
an adequate and informative feature extraction by transforming 
the time series with a *Fourier transform*. The magnitude peaks extracted 
from the transformations will represent our most informative features, 
taking into account especially those detected at *low compressor frequencies*, as well as one versus all correlations and autocorrelations. 
and autocorrelations. 

| <!-- -->    | <!-- -->    |  <!-- -->   |
|-------------|-------------|-------------|
<img src="https://github.com/giuseppedipoce/HACKATON-LHC-alert-detection/assets/93355495/2338924e-a32c-4f40-81d7-edbe81894367"> | <img src="https://github.com/giuseppedipoce/HACKATON-LHC-alert-detection/assets/93355495/dfd1ca77-4e4c-4db5-813b-8fa66fd753e7"> | <img src="https://github.com/giuseppedipoce/HACKATON-LHC-alert-detection/assets/93355495/46b9aa2c-2e85-415f-9905-62d3197600d6">

After over and undersampling we implement a logistic
regression with selected best parameters in cross validation. Note that we implelemented a *model agnostic permutations
feature importance* in order to filter the most importart variables and reduce the dimensionality of our data. 

## Short considerations about the results

The strong imbalance of input data made this hackathon a very compelling challenge. We can state that the low frequencies of the power spectrum extracted are very informative for the purpose of alert detection, however in order to improve our models we could try to eliminate the oversampling procedure and work better on the logistics regression weights. Please notice that this work has been done in 48 hours of hackaton.

## Used technologies
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## Content

`Hackathon.ipynb`: final notebook with the EDA and the final results obtained through our feature extraction and models;
`corr4hacka.rmd`: script (Rmarkdown) to derive correlations between timeseries;

`nice_plots.py`: functions for nice plots;


### Team ("🍫I Cioccolatosi🍫"): 
- Enrico Grimaldi ([Linkedin](https://www.linkedin.com/in/enrico-grimaldi18/) - [Github](https://github.com/Engrima18))
- Giuseppe Di Poce ([Linkedin](https://www.linkedin.com/in/giuseppe-di-poce-82a4ba14a/) - [Github](https://github.com/))
- Davide Vigneri ([Linkedin](https://www.linkedin.com/in/davide-vigneri-59a56021a/) - [Github](https://github.com/giuseppedipoce))
- Nicola Grieco ([Linkedin](https://www.linkedin.com/in/nicola-grieco-36a993233/) - [Github](https://github.com/nicolagrieco00))
