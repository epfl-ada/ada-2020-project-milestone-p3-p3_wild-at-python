
# Project Milestone 3: Linguistic Cues for Textual Classification
# Abstract

For the linguistics harbringers of betrayal, the authors try to predict if a betrayal is going to occur or not, using the following features of the messages:

![](P3\_Milestone.001.png)

However, we do notice two things that we can add to the analysis made in this paper:

- Time: The temporal relation between seasons, or the evolution of the features through time, may add a lot to the model in predictive power. Seasons evolve through time and things that have been said before might inuence things and events that will happen in the future.
- Linguistic cues: The features that directly allows to foretell betrayal are very implicit for us humans and we cannot do better than average. Thus, dening the features ourselves cannot give us the best give us a correlation result with the output. In modern day text handling or sentiment analysis, we let the model extract its own features from the text, and this usually gives very accurate results.

When we say text handling and time series we usually hear with it recurrent neural nets, which are perfect for the job because of their computation graph. Thus, we will try to use them to make some analyses on their results

# Research Questions  
- Can analysis using time series, like with RNNs, help improve the performance of the model made by the authors? 
- Can the features used by the authors generalize to analogous NLP classification problems with a dataset of Real and Fake news ? 
- Will the models perform better if we give them the freedom of learning their own features from the texts? 
# Proposed datasets
Our project consists on two parts, each with a diffrent dataset.
* The first dataset is the diplomacy game dataset that was provided with the paper 

* The second dataset is the Fake and real news dataset (https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset).  

This dataset contains two sets, a set of real news and another one of fake news. Both sets contain the same features, which are: 
* **text**: The actual text of the news article. 
* **title**: The title of the article.
* **subject**: Every article is classified in a type of subject either 'Government News' or 'Middle-east' or 'News' or 'US_News' or 'left-news' or 'politics' or 'politicsNews' or 'worldnews'.
*  **date**: date of publication of the article.


The  truthful  articles  were  obtained by  crawling  articles  from  Reuters.com  (News website).  As  for  the  fake  news  articles,  they  were  collected  from  different  sources.  The  fake  news articles  were  collected  from  unreliable  websites  that  were  flagged  by  Politifact  (a fact-checking organization in the USA) and Wikipedia. The dataset contains different types of articles on different topics, however,the majority of articles focuson political and World news topics.

# Methods

***Building the network:*** We plan on deploying the RNN (with LSTM layers) with the Keras library to answer the questions previously asked. The architectures of both RNNs are going to be specically tuned for each problem.

***Feature detection:*** The objective is to make a specially tuned architecture of RNNs for this problem. We will start rst with an architecture to observe the eect of adding time and then add another one that mixes the time factor with the automatically deduced linguistic cues. We will in fact use RNNs with LSTM layers to take advantage of their memory power for better predictions.

***Data analysis:*** We are interested in detecting new features in the messages and see the eect of time in the prediction. By analysing the results of our models we will see if there are others cues to detect betrayal that the authors didn't detect and use.

![](P3\_Milestone.002.png)

# Proposed timeline
1. First week  
- preprocess the diplomacy dataset   
- build the RNN model for the diplomacyy dataset and run it  
- analyse the results  
- Explore the second dataset  
2. Second week  
- preprocess the second dataset  
- extract the features from the second dataset  
- analyse the results  
- Implement an MLP model and train it with the collected features  
- first part of the data story  
3. Third week  
- Implement an MLP model and train it on the texts of the news dataset   
- Implement an RNN model an run it on the texts of the news dataset   
- Analyse and compre the results of the diffrent models 
- clean and merge the code
- Second part of data story  
- Film the video  

# Organization within the team
- preprocess the dimplomacy dataset, design the RNN model and run it (ana, zeineb, nizar)  
- Explore the new dataset, preprocess it and extract the features (zeineb)  
- Analyse the results and compare the features (zeineb, nizar)  
- Implement an MLP model and train it with the collected features  (zeineb )  
- Implement an MLP model and train it on the texts of the news dataset (nizar)  
- Implement an RNN model an run it on the texts of the news dataset (nizar)  
- Analyse and compre the results of the diffrent models ( zeineb, nizar)  
- data story (zeineb, nizar, ana)
- video (zeineb, nizar, ana)

# Project structure  
We split the code into several sections, to keep it clear and well organized. 

* **Diplomacy.ipynb**: the Dimplomacy file contains all the work we did on the diplomacy dataset (preprocessing + RNN model)
* **preprocess_coreNLP.ipynb**: this file contains the preprocessing of the news dataset and the sentiment analysis using the stanford coreNLP 
* **features_extraction.ipynb**: this file contains the feautues extraction of the news datasets 
* **Analysis_news.ipynb**: this file contains the analysis of all the features that we extracted for the news dataset and the MLP model that we trained on them 
* **Textual_analysis.ipynb**: this file  contains the textual analysis on the news dataset (MLP + RNN on the texts)
* **metrics.py**: file that contains methods to compute the metrics, they are used in several models thus we put them in a seperate file

**Note**: all the files are part of our project and we kindly ask you to correct them all.







