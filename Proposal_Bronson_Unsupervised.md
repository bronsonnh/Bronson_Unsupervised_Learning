# Sentiment Analysis from Album Reviews for Pink Floyd’s Dark Side of the Moon

By Nicholas Bronson

## Question/Need:

My client is a record label that is seeking to use Natural Language Processing in the analysis of album (LP), EP, and single record reviews for both artists on their label, and their peers. They believe that understanding listeners’ feelings and reviews can assist them in refining the music of the artists on their labels. They wish to assist the artists on their label in highlighting and capitalizing on what are perceived as areas of strength and improving areas of weakness in their upcoming releases.
My client wishes to see a proof of concept prior to committing to a longer-term project. For this initial project, they are looking to see how NLP can be used to analyze sentiments for what is widely regarded as a classic album, Pink Floyd’s Dark Side of the Moon. They have provided a dataset that contains a number of reviews of the album along with ratings for the majority of these reviews.

My client has two questions and these are as follows:

1) How can NLP be used to analyze listener sentiments from written reviews of music both qualitatively and quantitatively? 
2) What are listener sentiments on Pink Floyd’s Dark Side of the Moon, what are the perceived strengths and weaknesses of the album?  

## Data Description:

The dataset contains 1544 records, each one containing a written review of the album, with 1491 out of the 1544 reviews containing a numerical rating from 1-5, with 1 being the lowest score, and 5 being a perfect score. This dataset was acquired from Kaggle and it is a dataset that was scraped from users of rateyourmusic.com](https://rateyourmusic.com/), a site where users can provide reviews and ratings for albums. The reviews average roughly 138 words each. It appears the majority of the reviews are in English, however, there appear to be reviews in several other languages as well.

## Tools: 

For these analyses, I plan to use python including various libraries including Pandas, NumPy, Scikit-learn, NLTK, spaCy, matplotlib, and seaborn. I may include additional libraries or tools depending on the outcomes of initial exploration and analysis.

## MVP Goal: 

The minimum viable product for this project is an initial analysis of the major themes present in the reviews for the selected album. This will be created through topic modeling and will provide an overview of primary topics addressed in the reviews. Additionally, I will provide an overview of the breakdown of the number and percentage of positive and negative reviews, as well as terms associated with positive and negative reviews. 
