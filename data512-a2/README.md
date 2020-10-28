

# DATA 512 A2: Data Curation by Avani Bajaj


## Goal
For this assignment, we have identify potential sources of bias in a corpus of human-annotated data, and described some implications of those biases. 

The corpus you will use is called the Wikipedia Talk corpus, and it consists of three datasets. Each dataset contains thousands of online discussion posts made by Wikipedia editors who were discussing how to write and edit Wikipedia articles. Crowdworkers labelled these posts for three kinds of hostile speech: “toxicity”, “aggression”, and “personal attacks”. Many posts in each dataset were labelled by multiple crowdworkers for each type of hostile speech, to improve accuracy.

### Dataset Sources
The Datasets used in the analysis are available in Figshare:
1. Toxicity - Datasets [here](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Toxicity/4563973)
2. Aggression - Datasets [here](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Aggression/4267550)
3. Personal Attack - Datasets [here](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Personal_Attacks/4054689)

More details about the data files and its schema can be found [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release#Toxicity)
These datasets are used for a creating a project called [Conversation AI](https://conversationai.github.io/). These models are freely available for use via the [Perspective API](https://www.perspectiveapi.com/#/home) <br />


## About

We explored the data and conducted some analysis on the demographic data for the 3 segments we had - toxic, aggressive and attack. Demographics can play a huge role on how the worker annotate the dataset. The features we looked into include - gender, region, education, age

**Dataset for this analysis**
To provide a wholesome picture of the corpus data, I would be doing this analysis on all the three datasets. This would provide a deeper understanding of bias compared to picking only one or two datasets.
The data is fetched directly from the location/URL link. The data is heavy and all the dataset may or may not be present in the github repository

### Output

The output from the analysis are also stored in the output folder.

## Repository content
- data - contains all input data files used in notebook
- output - contains all graphs and analysis produced by notebook
- Python notebook containing all code and information: *DATA512-a2.ipynb*


## Reproduce
This repository should be straight forward to reproduce. Simply download the python notebook file and run it in your python environment. The code uses standard libraries and generates all outputs without any other manual step.

## License
The repostory follows MIT License as mention [here](https://github.com/avani-bajaj/DATA512/blob/main/data512-a2/LICENSE).
