# CMSC 516 NER War Tweets

## Content

| Section | Description |
|-|-|
| [Project description](#project_description) | Detailed description of the project |
| [Installation](#installation_instructions) | How to install the package |
| [Overview](#overview) | Overview of the package |
| [Method](#method) | Method used for codes |
| [Doc](#doc) |  Detailed documentation |
| [Notebooks](#notebooks) | Introduction on the provided Jupyter Notebooks |
| [Data](#data) | Data used to train the models |
| [Results](#results) | Results of the models |

## Project Description
For this project we have set up 2 different methods set up to determine Named Entity Recognition of News headlines pertaining to War and comparing them with tweets of current war news. Our first method utilized the BERT model with PyTorch to provide an accuracy score of 91% for our test data. We also utilized a Keras model with BiLSTM to provide accuracy, precision, recall, f1, and support scores.

We use Tweepy to grab any tweets related to the hashtags of current wars. This includes: 1.Israel
2.Palestine
3.Russia
4.Syria
5.Ukraine
6.UkraineRussiaWar

In both projects we make use of the same dataset in different formats, sentence separated and word separated, that is originally provided from Kaggle for NER research.

Our Notebooks will pull this raw data from the Github repository and separate it into 80% for training, 10% for developing, and 10% for testing. After the data is separated the Notebooks will train their respective models and output their scores on the test data once training completes.


## Overview


## Installation and Usage Instructions


## Method


## Data


## Doc


## Notebooks


## Results


## Discussion


## Future Work

