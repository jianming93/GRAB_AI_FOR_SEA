# GRAB_AI_FOR_SEA
This repo contains a few files which are:
1) EDA jupyter notebook for ease of viewing graphs and commenting
2) Training py file
3) Test py file
4) Raw data provided from the Grab itself
5) 

# Considerations for models
Initially, I considered using VAR for the prediction of the demand. However, after considering the availability of sufficient amount of data and considering the possibility of possible relationships between geohashs, I've decided to use a machine learning model instead.
Despite the idea of possiblity using a neural network like RNN to predict, I've decided to adopt a random forest model instead mainly due to speed. I will elaborate on this more in the later section

# Building the model
When first started, I wanted to try using a gradient boosted model. However, after trying out for a while, I considered to drop it due to speed. As it takes time for it to converge, while possibly attaining greater accuracy, running the iterations to get a good convergence without overfittin is a lot more time consuming than expected. As I believe since the intervals for the prediction of demand is in 15 mintes, there is a need to predict the data quickly. This lack of luxury of time thus changed my approach to adopt a random forest instead (Same reasoning to why I did not use a neural network). However, for my own learning experiences, I also used the lightgbm package to build my random forest model.

# Parameters tuning
From what I've gathered online (as I am new to using random forest more in depth), I've optimised based on these parameters:
1) Number of leaves
2) Minimum data per leaf
3) Max Bins
4) Max depth
The rest of the parameters which can be found in the code are static

# Things to improve
1) Hyparameter tuning more
2) Feature engineering to a greater extent
