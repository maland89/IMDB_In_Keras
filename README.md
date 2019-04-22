## Introduction

In this notebook, we analyzed a dataset from IMDB and use it to predict the sentiment analysis of a review.
In this lab, the data were preproceed and we were in charge of building and training the model in Keras.

## The dataset

This lab uses a dataset of 25,000 [IMDB](https://www.imdb.com/) reviews. Each review comes with a label. A label of 0 is given to a negative review, and a label of 1 is given to a positive review. The goal of this lab is to create a model that will predict the sentiment of a review, based on the words in the review. You can see more information about this dataset in the [Keras](https://keras.io/datasets/) website.

Now, the input already comes preprocessed for us for convenience. Each review is encoded as a sequence of indexes, corresponding to the words in the review. The words are ordered by frequency, so the integer 1 corresponds to the most frequent word ("the"), the integer 2 to the second most frequent word, etc. By convention, the integer 0 corresponds to unknown words.

Then, the sentence is turned into a vector by simply concatenating these integers. For instance, if the sentence is "To be or not to be." and the indices of the words are as follows:
* "to": 5
* "be": 8
* "or": 21
* "not": 3

Then the sentence gets encoded as the vector ```[5,8,21,3,5,8]```

## Getting Started

You can download a copy of the project from GitHub [here](https://github.com/maland89/IMDB_In_Keras.git) and then run a Jupyter server locally with [Anaconda](https://www.anaconda.com/download/).

1. Open a terminal and clone the project repository:
```
$ https://github.com/maland89/IMDB_In_Keras.git
```

3. Switch to the project folder and create a conda environment (note: you must already have Anaconda installed):
```
$ cd IMDB_In_Keras
IMDB_In_Keras/ $ conda env create -f IMDB_In_Keras.yaml
```

4. Activate the conda environment, then run the jupyter notebook server. (Note: windows users should run `activate IMDB_In_Keras`)
```
IMDB_In_Keras/ $ source activate IMDB_In_Keras
(IMDB_In_Keras) IMDB_In_Keras/ $ jupyter notebook
```

Depending on your system settings, Jupyter will either open a browser window, or the terminal will print a URL with a security token. If the terminal prints a URL, simply copy the URL and paste it into a browser window to load the Jupyter browser. Once you load the Jupyter browser, select the project notebook (IMDB_In_Keras.ipynb) and follow the instructions inside to complete the project.
