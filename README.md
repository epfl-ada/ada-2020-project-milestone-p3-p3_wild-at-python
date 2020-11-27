
#1  Title

Linguistic harbringers of betrayal

#2  Abstract

For the linguistics harbringers of betrayal, the authors try to predict if a betrayal is going to occur or not, using the following features of the messages:

![](P3\_Milestone.001.png)

However, we do notice two things that we can add to the analysis made in this paper:

- Time: The temporal relation between seasons, or the evolution of the features through time, may add a lot to the model in predictive power. Seasons evolve through time and things that have been said before might inuence things and events that will happen in the future.
- Linguistic cues: The features that directly allows to foretell betrayal are very implicit for us humans and we cannot do better than average. Thus, dening the features ourselves cannot give us the best give us a correlation result with the output. In modern day text handling or sentiment analysis, we let the model extract its own features from the text, and this usually gives very accurate results.

When we say text handling and time series we usually hear with it recurrent neural nets, which are perfect for the job because of their computation graph. Thus, we will try to use them to make some analyses on their results

**3  Research Questions**
- What is the eect of time on the ecien cy of model in foretelling betrayal ?
- What if we add automatic feature extraction ? Does this improve the performance of the model ?
- Given we only have 500 samples can we get our RNN to converge if correctly regularized and we use certain techniques such as super convergence or other ?
**4  Proposed datasets**

In our case the only data available is the one that came with the paper. No augmentation can be done, however additional preprocessing will be performed.

**5  Methods**

The objective is to make a specially tuned architecture of RNNs for this problem. We will start rst with an architecture to observe the eect of adding time and then add another one that mixes the time factor with the automatically deduced linguistic cues. We will in fact use RNNs with LSTM layers to take advantage of their memory power for better predictions.

![](P3\_Milestone.002.png)

We plan on deploying the RNN (with LSTM layers) with the Keras library to answer the questions previously asked. The architectures of both RNNs are going to be specically tuned for each problem.

**6  Proposed timeline**
- First we preprocess the data
- Design the rst RNN and build it.
- Run the RNN to observe the eects of adding time.
- Perform statistical analysis on the results and add some comparison plots between our results and the paper's results.
- First part of data story
- Design the second RNN and build it.
- Run the RNN to observe the eects of self learned linguistic cues.
- Perform statistical analysis on the results and add some comparison plots between our results and the paper's results and the our previous results.
- Second part of data story
- Write the report
- Film the video
**7  Organization within the team**
- Design of both RNNs (ana, nizar, zeineb)
- Implementation of the rst RNN (nizar)
- Implementation of second RNN (ana + zeineb)
- Statistical analysis + plots of the rst RNN (nizar)
- Statistical analysis + plots of the second RNN (zeineb)
- report (ana, nizar, zeineb)
- video (ana, nizar, zeineb)
**8  Questions to the TAs**

Q: We still don't know how much time it will take us to build the RNN models and run them. Our goal is to build the two RNNs and do analysis on both of them, but if the task appears to be very time consuming and end up not having enough time to do both of them, is it a problem if we only do the rst one in this case?
PAGE4
