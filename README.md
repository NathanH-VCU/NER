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

This is our approch for this project and how we divided the code tasks into sub-tasks.
![image](https://user-images.githubusercontent.com/83011466/204411284-da597fb9-fd33-4070-8f97-3522c8fbf0a0.png)


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

Another Data that we used is the <strong>MIT public Movie Corpus</strong> for Movies Reviews. 
https://groups.csail.mit.edu/sls/downloads/movie/ 

This data is a semantically tagged training and testing corpus in BIO format. The eng corpus (engtrain and engtest are available in the SRC folder).

![image](https://user-images.githubusercontent.com/83011466/204407413-0953b61d-11fe-4e41-af4d-f6f4b11330cd.png)

<strong>Data Training and Validation Split </strong>

The MIT public movie corpus was divided into a training set of 90% and 10% for validation set.

<strong>NER Tags and IOB Format </strong>
  
Both the train and test datasets are single files containing movie-related text where each word has a NER tag specifying it as one of the following entities.
The NER tag follows a special format used widely in NER literature called IOB format(Inside,Outside and Beginning Format).

<strong>O:</strong> This Tag means the word is not part of the entity
    
<strong>B: </strong> this tag means the word is either a single word entity name or else the first word in a multi-word entity name
    
<strong>I:</strong> this tag means the word is part of a ulti-word entity but is not the first word in the full entity name 
    

## Doc


## Notebooks

<strong>- NER_Nourchene_final_code.ipynb </strong> is the code for NER recognition with MIT public dataset using Bert with Pytorch and Adam optimizer.

<strong>- NER_using_BERT_with_PyTorch.ipynb </strong> is the code for NER recognition with KAGGLE dataset using Bert with Pytorch, CNN and SGD optimizer.

<strong>- NER_using_LSTM_with_Keras.ipynb </strong> is the code for NER recognition with KAGGLE dataset using LSTM with Keras.


## Results

<strong>1. MIT dataset :</strong>

<strong>Training Loss</strong>

![image](https://user-images.githubusercontent.com/83011466/204408854-f1078e61-de2c-4f42-bd15-d189f15c36cd.png)

The loss value decreases each epoch and at the end of the epoch 5, the loss value becomes really small. The training performed well with no overfiting.
is a phenomenal result

<strong>Classfication Report</strong>

![image](https://user-images.githubusercontent.com/83011466/204411658-73294ea2-dc91-4fe6-8f86-6ea14d9bd73c.png)

Our model got the F-1 score of 94.4 %


## Discussion

As we worked on different Machine Learning algorithms: CNN, LSTM, BiLSTM and also using different optimizerslike Adam and SGD.
With Bert Pytorch LSTM and Adam optimizer we got <strong>94% accuracy</strong> which is a good result compared to<strong> 88% </strong>accuracy with Adam optimizer for CNN.
![image](https://user-images.githubusercontent.com/83011466/204414572-9d56a9a8-f84a-40c8-9fdd-adc729c135e9.png)



## Future Work

