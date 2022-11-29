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

- B-geo 	 37644 	 23.43 %
- B-gpe 	 15870 	 9.878 %
- B-per 	 16990 	 10.575 %
- I-geo 	 7414 	 4.615 %
- B-org 	 20143 	 12.537 %
- I-org 	 16784 	 10.446 %
- B-tim 	 20333 	 12.655 %
- B-art 	 402 	   0.25 %
- I-art 	 297 	   0.185 %
- I-per 	 17251 	 10.737 %
- I-gpe 	 198 	   0.123 %
- I-tim 	 6528 	 4.063 %
- B-nat 	 201 	   0.125 %
- B-eve 	 308 	   0.192 %
- I-eve 	 253 	   0.157 %
- I-nat 	 51 	   0.032 %

For our twitter data we are using tweepy to pull from the twitter api all tweets with the tags “Israel”, “Palestine”, “Russia”, “Syria”, “Ukraine”, “UkraineRussiaWar”. This includes about 200 tweets for each tag.

Another Data that we used is the MIT public MIT Movie Corpus for Movies Reviews. 
https://groups.csail.mit.edu/sls/downloads/movie/ 
This data is a semantically tagged training and testing corpus in BIO format. The eng corpus (engtrain and engtest are available in the SRC folder)
![image](https://user-images.githubusercontent.com/83011466/204407413-0953b61d-11fe-4e41-af4d-f6f4b11330cd.png)


## Doc


## Notebooks


## Results


## Discussion


## Future Work

