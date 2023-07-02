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


## Model selection

Our team developed, in the light of the data handled
an adequate and informative feature extraction by transforming 
the time series with a *Fourier transform*. The magnitude peaks extracted 
from the transformations will represent our most informative features, 
taking into account especially those detected at *low compressor frequencies*, as well as one versus all correlations and autocorrelations. 
and autocorrelations. After over and undersampling we implement a logistic
regression with selected best parameters in cross validation. Note that we implelemented a *model agnostic permutations
feature importance* in order to filter the most importart variables and reduce the dimensionality of our data. 

## Short considerations about the results

The strong imbalance of input data made this hackathon a very compelling challenge. We can state that the low frequencies of the power spectrum extracted are very informative for the purpose of alert detection, however in order to improve our models we could try to eliminate the oversampling procedure and work better on the logistics regression weights. Please notice that this work has been done in 48 hours of hackaton.

## Used technologies
![repo](https://github.com/giuseppedipoce/HACKATON-Stat.-Learning-/assets/114066138/a09d2bfa-4348-4286-8a1a-538f3d9ab5f5)




### Team ("🍫I Cioccolatosi🍫"): 
- Enrico Grimaldi ([Linkedin](https://www.linkedin.com/in/enrico-grimaldi18/) - [Github](https://github.com/Engrima18))
- Giuseppe Di Poce ([Linkedin](https://www.linkedin.com/in/giuseppe-di-poce-82a4ba14a/) - [Github](https://github.com/)
- Davide Vigneri ([Linkedin](https://www.linkedin.com/in/davide-vigneri-59a56021a/) - [Github](https://github.com/giuseppedipoce)
- Nicola Grieco ([Linkedin](https://www.linkedin.com/in/nicola-grieco-36a993233/) - [Github](https://github.com/nicolagrieco00)
