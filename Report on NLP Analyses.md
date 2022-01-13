
# Decoding Album Reviews for Pink Floyd’s Dark Side of the Moon: Sentiment Analysis using NLP

By Nicholas Bronson

## Abstract:

This project seeks to assist my client, a record label, in analyzing music reviews they have scraped from rateyourmusic.com. My client wants to better understand reviewer sentiments and wants to investigate the usage of natural language processing (NLP) of reviews to understand if and how these processes can provide valuable insights. Specifically, they are looking to better understand the characteristics, perceived strengths, and weaknesses of albums, singles, and EPs in genres that the label’s artists cater to. The end goal is to guide the sound of the artists on their label, and increase their levels of appeal by using insights extracted from reviews. Prior to launching a larger scale NLP project across artists and genres, they wish to see a proof-of-concept in the form of an analysis of a dataset containing reviews of Pink Floyd’s Dark Side of the Moon. 

To conduct this analysis review data was tokenized, and analyzed using several unsupervised learning methods to understand topics and broad-strokes information about reviewer sentiments. Following this, classification modeling was conducted in order to construct a model that can identify whether reviews are positive or negative given the language and topics present in the data. 

## Design: 

The goal of this project is to use unsupervised learning to uncover inisghts about album reviews. This is done using NLP, and it is carried out on Pink Floyd's classic album Dark Side of the Moon, the 6th best selling album of all time by total certified copies sold. Finding trends and topics within the language used in the reviews is the first phase of the project, subsequently, supervised learning is used to create a model that can predict weather reviews are negative or postivie from the language alone. This model is useful for identifying sentimients for unlabeled reviews. 

## Data:

The data is a 1547 row dataset scraped from [rateyourmusic.com](rateyourmusic.com) on October 15th, 2021 that I acquired from Kaggle. The reviews contain an average of 138 words each. Out of these reviews, 1494 have a rating associated with the review. The average rating, out of 5 points, is 4.4 across reviews. 

## Algorithms:

To begin the analysis, reviews were ingested into python, and exploration was used to determine characteristics of the data. Following this, basic preprocessing was initiated in order to tokenize data and clean it for analysis. Both count vectorization and TF-IDF vectorization were examined, with both techniques proving useful. Several tools including NMF, LDA, PCA, and K-means clustering were used for dimensionality reduction and topic modeling. NMF was chosen as the primary tool used to analyze the text data after the second round of more rigorous pre-processing in which additional stop words were added, including terms like “Pink Floyd” and the album’s name which could be present in any type of review and did not provide valuable insights. Additionally, the threshold for upper and lower boundaries that determined which words were analyzed was adjusted to pare down the dataset.    

Breaking the data into 8 topics using an NMF model led to 4 interpretable topics:

a) Extremely lengthy, highly positive, and analytical reviews
b) Non-English reviews (Italian, Spanish, and Portuguese reviews were identified) 
c) Short reviews labeling the album a “classic” or the “greatest album of all time” 
d) Reviews noting the album is too overrated, or perhaps good but overrated

These groupings provide insight into overall reviewer sentiments of the strengths of the album, as well as the perception that the album is perhaps overrated, but rarely labeled as unenjoyable to listen to. 

Following the use of unsupervised learning, several supervised learning methods were used to analyze ratings that accompanied reviews. Reviews were broken down into the category “Positive” if their rating was 3 or greater, with reviews lower than 3 being classified as “Negative.” All of the models used had difficulty predicting true negatives but did a relatively good job at predicting actual positives, this was most likely due to the unbalanced nature of the data. A random forest model produced the best ability to capture true negatives as well as true positives, with scores as follows:

Accuracy: 0.904, Recall: 0.975, Precision: 0.923, F1: 0.948

## Tools:

The tools used for this project included Python, packages such as NLTK, Pandas, Numpy, Sklearn. Seaborn, pyLDAvis, and scattertext were used for visualization.  

## Communications:

Communication for this project is in the form of a Google slides deck. This slide deck includes an overview of the analyses conducted, findings, recommendations, and an outline of next steps. I have also provided an accompanying set of Jupyter notebooks that provide additional insight into the analyses.
