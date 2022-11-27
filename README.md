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

We use Tweepy to grab any tweets related to the hashtags of current wars. This includes:
- Israel
- Palestine
- Russia
- Syria
- Ukraine
- UkraineRussiaWar

In both projects we make use of the same dataset in different formats, sentence separated and word separated, that is originally provided from Kaggle for NER research.

Our Notebooks will pull this raw data from the Github repository and separate it into 80% for training, 10% for developing, and 10% for testing. After the data is separated the Notebooks will train their respective models and output their scores on the test data once training completes.


## Installation and Usage Instructions
This repo was tested on Python 2.7 and 3.5+ 

This project was built and tested in Google Colab. It can be ran the same way. 

To run this project yourself:
1. Follow this link to the Github-to-Colab .ipynb file - [Github to Colab - NER_using_LSTM_with_Keras](https://githubtocolab.com/NathanH-VCU/NER/blob/main/NER_using_LSTM_with_Keras.ipynb) and [Github to Colab - NER_using_BERT_with_PyTorch] https://githubtocolab.com/NathanH-VCU/NER/blob/main/NER_using_BERT_with_PyTorch.ipynb
2. Click Runtime
3. Click Run All
4. Authorize the notebook
5. Wait until the process finishes, our tests took about 40 minuets with our sample data.

## Overview


## Method
1. For BERT with PyTorch : 
-	Feature representation : Bert contextual embedding
-	Python Algorithm : Standard PyTorch training
-	Dataset : Kaggle NER dataset, sentence separated
2. For Keras with BiLSTM:
- Feature representation : TensorFlow Keras Embedding
- Algorithm : Stochastic Gradient Descent
- Dataset : Kaggle NER dataset, word separated


## Data
For our data we are utilizing a dataset provided through Kaggle called “NER Data” which contains a list of news article headlines and a list of each words’ labels. In total the data contains 47,960 headlines and their labels as well as 17 different labels including the O:
![plot histogram of tags](https://github.com/NathanH-VCU/NER/raw/main/src/assets/newplot.png)

- B-geo&emsp;&emsp;37644&emsp;&emsp;23.43%
- B-gpe&emsp;&emsp;15870&emsp;&emsp;9.878%
- B-per&emsp;&emsp;16990&emsp;&emsp;10.575%
- I-geo&emsp;&emsp;7414&emsp;&emsp;4.615%
- B-org&emsp;&emsp;20143&emsp;&emsp;12.537%
- I-org&emsp;&emsp;16784&emsp;&emsp;10.446%
- B-tim&emsp;&emsp;20333&emsp;&emsp;12.655%
- B-art&emsp;&emsp;402&emsp;&emsp;0.25%
- I-art&emsp;&emsp;297&emsp;&emsp;0.185%
- I-per&emsp;&emsp;17251&emsp;&emsp;10.737%
- I-gpe&emsp;&emsp;198&emsp;&emsp;0.123%
- I-tim&emsp;&emsp;6528&emsp;&emsp;4.063%
- B-nat&emsp;&emsp;201&emsp;&emsp;0.125%
- B-eve&emsp;&emsp;308&emsp;&emsp;0.192%
- I-eve&emsp;&emsp;253&emsp;&emsp;0.157%
- I-nat&emsp;&emsp;51&emsp;&emsp;0.032%

For our twitter data we are using tweepy to pull from the twitter api all tweets with the tags “Israel”, “Palestine”, “Russia”, “Syria”, “Ukraine”, “UkraineRussiaWar”. This includes about 200 tweets for each tag.


## Doc


## Notebooks


## Results


## Discussion


## Future Work

