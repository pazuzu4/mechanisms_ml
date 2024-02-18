# Mechanisms of Injury Prediction

## Project Description

NEISS is a popular data source for injury related research, but the mechanism of injury labeling process is very manual. [Using data from this research on pickleball and tennis injuries among seniors](https://pubmed.ncbi.nlm.nih.gov/33934725/) from 2010-2019, A decision tree based model is used to classify the mechanism of injury from 2020 to 2022

## Table of Contents

-   [Installation](#Installation)
-   [Usage](#Usage)
-   [Data](#Data)
-   [Models](#Models)
-   [Contributing](#Contributing)
-   [References](References)

## Installation {#Installation}

To be added for future commits, not sure how this works yet.

## Usage {#Usage}

Code and examples will be added in the next commit.

## Data {#Data}

Documentation, information, and downloads for the NEISS data can be found [here](https://www.cpsc.gov/Research--Statistics/NEISS-Injury-Data).

The mechanism of injury used in the referenced paper is called "primary_mechanism". This is used as the Y variable in the decision tree modeling.

More examples and information will be added

## Models {#Models}

Much more details to come here, but there were a few types of models trained. and compared. Some models used adjustments for survey weights, those will be compared in a future commit. All models were trained on two sets of data, one would use total word counts and one which used word detection. Models trained on those two different datasets almost always agreed, but the case is where they disagreed are interesting. You can find an excel output of all the cases where those two model disagrees in the disagree_rows in the csv.

## Contributing {#Contributing}

I want this to be open source and as transparent as possible, any contributions are appreciated.

## References {#References}

-   For the foundation of the NEISS data labeling process automation in this project, see the study available at [PubMed](https://pubmed.ncbi.nlm.nih.gov/33934725/),
-   Documentation, information, and downloads for the NEISS data can be found [here](https://www.cpsc.gov/Research--Statistics/NEISS-Injury-Data).
