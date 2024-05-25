# Mechanisms of Injury Prediction

## Project Description

NEISS is a popular data source for injury related research, but the mechanism of injury labeling process is very manual. In this project, various neural networks and machine learning methods are built to predict the primary mechanism of injury [using data from this research on pickleball and tennis injuries among seniors](https://pubmed.ncbi.nlm.nih.gov/33934725/) from 2010-2019. The models are built using basic the variables provided by NEISS, including the text narrative which describes how the injury happens. Data from 2020 to 2022 are also available for evaluation.

## Table of Contents
-   [Overview](#Overview)
-   [Usage](#Usage)
-   [Data](#Data)
-   [Contributing](#Contributing)
-   [References](References)

## Overview

Currently the decision tree model, which uses XGBoost, performs the best at predicting the primary mechanism of injury with 89.25% accuracy on an unbiased test set. That outperforms the 48.5% "no information rate" and is roughly in line with the ~90% cross validated accuracy.

Neural networks built using Keras are now approaching the accuracy of the XGBoost models at 87.5%, up from ~75% originally. The networks use dense word embeddings to process the text directly rather than using indicator or dummy variables. Pre-trained word embeddings did not perform as well as when they were learned via the NEISS data, which is a little surprising given the sample size limitations. These models will likely be the highest performing, eventually.

A deeper analysis into the models and results can be found in the "Results and Evaluation" R file in the "Results" folder.

## Data

Documentation, information, and downloads for the NEISS data can be found [here](https://www.cpsc.gov/Research--Statistics/NEISS-Injury-Data). The mechanism of injury used in the referenced paper is called "primary_mechanism". This is used as the Y variable in the decision tree modeling.

There are a lot of datasets used for this project at various stages. Below is a summary of some of the important ones:

- Training and test sets
	- All training and test sets can be found in a subfolder of the "data_to_model" folder
	- Train & test sets use a stratified random sample given the class imbalance in the data
	- The Keras model does some other minor data prep in its modeling file
- Prediction data 
	- Model outputs can be found in the "Prediction Data" folder under "Results"
- Unlabeled new data from 2020-2022
	- A fun aspect of this data is it's continuously collected so we can use it on new data
	- Model-ready new data is available in the "data_to_model" folder
	- These may one day be updated with true labels as well

Note that this mostly focuses on the data used in the modeling and prediction process. But all data cleaning and processing code is available in the "Data Prep" subfolder of the "Code" folder.
## Contributing

I want this to be open source and as transparent as possible, any contributions are appreciated.

## References

-   For the foundation of the NEISS data labeling process automation in this project, see the study available at [PubMed](https://pubmed.ncbi.nlm.nih.gov/33934725/),
-   Documentation, information, and downloads for the NEISS data can be found [here](https://www.cpsc.gov/Research--Statistics/NEISS-Injury-Data).
