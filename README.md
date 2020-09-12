# Cryptocurrency-NLP-Sentiment-Analysis
This project will apply several Natural Language Processing techniques to evaluate the current sentiment on Bitcoin and Ethereum from news articles.

## Sentiment Analysis

### Process:
1) All recent articles for Bitcoin and Ethereum were retrieved using the News API.
2) Then all articles were added to a DataFrame with sentiment scores (compound, positive, neutral and negative) on each text added as columns.
3) Then using the describe function on the Dataframe we can see the general sentiment on each coin.

### Conclusions

***Which coin had the highest mean positive score?***

A: Bitcoin had the highest mean postive score between the two coins at 0.075

***Which coin had the highest compound score?***

Ethereum had the highest compound score, with a max score of 0.7579

***Which coin had the highest positive score?***

A: Ethereum also had the highest postive score, with a max positive score of 0.209

## Natural Language Processing

### Tokenize
First I created a function to take in each text in the earlier created DataFrames and: (i) lowercase each word; (ii) remove punctuation; (iii) remove stop words; (iv) lemmatize and tokenize each word into a separate column

### NGrams and Frequency Analysis
Next, I looked at the ngrams and word frequency for each coin. I used the NLTK library to produce the ngrams for N = 2. Then I listed the top 10 words for each coin.

### Word Clouds
Finally, I generated word clouds for each coin to summarize the news for each coin, see below.

***Bitcoin Word Cloud:***

![BTC_wc](Images/BTC_Word_Cloud.PNG)

***Ethereum Word Cloud:***

![ETH_wc](Images/ETH_Word_Cloud.PNG)

### Named Entity Recognition
In this section, I built a named entity recognition model for both coins and visualized the tags using SpaCy.
