# Project Milestone 3: Linguistic Cues for Textual Classification
# Abstract

Under the scope of EPFL's ADA class project, we will perform a creative extension on the paper Linguistic Harbingers of Betrayal. In this project we will work on Natural Language Processing (NLP) and more specially on Linguistic cues. As we will present to you in the next section, the authors of the paper worked on the messages of the diplomacy game and extracted some features to do some analysis and then train a simple model to perform a complex task, even for humans, which is detecting betrayal. To extend this work we will first try to train more complex and adapted models for this kind of tasks, like RNNs to see how they perform and draw some conclusions from the results. Then we will extend this work to another and completely different dataset, a dataset of news. The goal is to try and see if the same features can be used for various NLP examples.
 

# Research Questions  
- Can analysis using time series, like with RNNs, help improve the performance of the model made by the authors? 
- Can the features used by the authors generalize to analogous NLP classification problems with a dataset of Real and Fake news? 
- Will the models perform better if we give them the freedom of learning their own features from the texts? 
# Proposed datasets
Our project consists of two parts, each with a different dataset.
* The first dataset is the diplomacy game dataset that was provided with the paper 

* The second dataset is the Fake and real news dataset (https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset).  

This dataset contains two sets, a set of real news and another one of fake news. Both sets contain the same features, which are: 
* **text**: The actual text of the news article. 
* **title**: The title of the article.
* **subject**: Every article is classified in a type of subject either 'Government News' or 'Middle-east' or 'News' or 'US_News' or 'left-news' or 'politics' or 'politicsNews' or 'worldnews'.
*  **date**: date of publication of the article.


The  truthful  articles  were  obtained by  crawling  articles  from  Reuters.com  (News website).  As  for  the  fake  news  articles,  they  were  collected  from  different  sources.  The  fake  news articles  were  collected  from  unreliable  websites  that  were  flagged  by  PolitiFact  (a fact-checking organization in the USA) and Wikipedia. The dataset contains different types of articles on different topics, however, the majority of articles focus on political and World news topics.

# Methods

***Building the network:*** We plan on deploying the RNN with the Keras library to train it on the diplomacy features.

***Data collection:*** To reproduce the analysis done in Linguistic Harbingers of Betrayal paper we need to preprocess the news dataset and extract the same features from it.

***MLP with features*** We will run an MLP on the extracted features and analyze the results 

***Textual analysis:*** We will run two models, MLP and RNN with LSTM, on the news texts given them the freedom to learn their own features and then compare the results with the previous model

![](P3\_Milestone.002.png)

# Proposed timeline
1. First week  
- preprocess the diplomacy dataset   
- build the RNN model for the diplomacy dataset and run it  
- analyze the results  
- Explore the second dataset  
2. Second week  
- preprocess the second dataset  
- extract the features from the second dataset  
- analyze the results  
- Implement an MLP model and train it with the collected features  
- first part of the data story  
3. Third week  
- Implement an MLP model and train it on the texts of the news dataset   
- Implement an RNN model an run it on the texts of the news dataset   
- Analyze and compare the results of the different models 
- clean and merge the code
- Second part of data story  
- Film the video  

# Organization within the team
- preprocess the diplomacy dataset, design the RNN model and run it (ana, zeineb, nizar)  
- Explore the new dataset, preprocess it and extract the features (zeineb)  
- Analyze the results and compare the features (zeineb, nizar)  
- Implement an MLP model and train it with the collected features  (zeineb )  
- Implement an MLP model and train it on the texts of the news dataset (nizar)  
- Implement an RNN model an run it on the texts of the news dataset (nizar)  
- Analyze and compare the results of the different models ( zeineb, nizar)  
- data story (zeineb, nizar, ana)
- video (zeineb, nizar, ana)

# Project structure  
We split the code into several sections, to keep it clear and well organized. 

* **Diplomacy.ipynb**: the Diplomacy file contains all the work we did on the diplomacy dataset (preprocessing + RNN model)
* **preprocess_coreNLP.ipynb**: this file contains the preprocessing of the news dataset and the sentiment analysis using the stanford coreNLP 
* **features_extraction.ipynb**: this file contains the features extraction of the news datasets 
* **Analysis_news.ipynb**: this file contains the analysis of all the features that we extracted for the news dataset and the MLP model that we trained on them 
* **Textual_analysis.ipynb**: this file  contains the textual analysis on the news dataset (MLP + RNN on the texts)
* **metrics.py**: file that contains methods to compute the metrics, they are used in several models thus we put them in a separate file


**Note**: all the files are part of our project and we kindly ask you to correct them all.

**Note**: we included the files in a zip format please unzip them before running the code, you also need to download the file from glove file from http://nlp.stanford.edu/data/glove.twitter.27B.zip.


# Data story  
You can find our data story in the following link https://zeineb111.github.io/Linguistic-cues-for-Textual-classification/




 
