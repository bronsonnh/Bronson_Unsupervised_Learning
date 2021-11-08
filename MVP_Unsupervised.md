# Minimum Viable Product: Sentiment Analysis from Album Reviews for Pink Floyd’s Dark Side of the Moon

By Nicholas Bronson

In initial investigation of the provided reviews I was able to tokenize the words in the reviews and break the reviews down into 10 topics by use of Latent Dirichlet allocation. Please see below:

![Topic_1](https://github.com/bronsonnh/Bronson_Unsupervised_Learning/blob/main/LDA_topic_1.png)

![Topic_3](https://github.com/bronsonnh/Bronson_Unsupervised_Learning/blob/main/LDA_topic_3.png)


Topic one appears to contain positive reviews judging by the high number of occurances of the word "great." On the other hand, topic 3 contains a number of reviews with the word "bad," which shows that that topic may contain negative reviews. 

At the moment, this model is quite basic, and the data could likely use to be processed again, as certain words like "album" and "music" appear frequently but don't necssarily provide much value. These words could perhaps be removed without losing any signficiant value, which would allow deeper analysis of terms that may be of more value in understanding listener sentiments. Ultimately, I aim to refine this model and break the reviews down into topics that more closely demonstrate reviewer sentiments. 
