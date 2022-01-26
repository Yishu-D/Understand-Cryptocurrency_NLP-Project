# Understand-Cryptocurrency_NLP-Project
### Yishu Dai
#### January 25, 2021
---

#### Abstract
  
The goal of this project is to analyze Tweets about top 5 cryptocurrencies using Natural Language Processing (NLP) and topic modeling techniques. The dataset of tweets was obtained using [Twitter API](https://developer.twitter.com/en/docs/twitter-api). The tweets data was preprocessed using RegEx and the NLTK library. Topic modeling was performed with Sci-kit Learn. Due to the randomness of tweets and cryptp, the final analysis is done manually by analyzing sample tweets.


#### Design

Cryptocurrency has gained tremendous popularity in the past few years. With more crypto tokens and NFTs popping up, I started wondering what are people talking about cryptos in social media? Twitter, Discord and Telegram are the most common tools used by crypto community, since the latter two are not public plarforms, I decided to look into tweets that inlclude text or hashtags of the top 5 cryptocurrencies. I hope to get a better understanding of people's thoughts and interests in crypto and provide some insights to my new job (a blockchain company)


The general pipeline of the process is: data gathering, cleanup, text preprocessing, topic modeling, and visualization. 

#### Data
  
The datas was was obtained using [Twitter API](https://developer.twitter.com/en/docs/twitter-api). 10,000 Tweets were scrapped using 'bitoin', 'ethereum', 'binance', 'tether' and 'solana' as the keywords. The data was generated on Jan 16th. 10 topics of each crypto were created and analyzed. 

  
#### Algorithms
  
*Data Cleanup* 
  
  The first issue with the data is there are a significant amount of repeating tweets. Each topic's dataset was process to delete duplicated tweeets before further processing. 
  
*Text Preprocessing*
  
  Extensive text preprocessing was done for efficient and productive topic modeling. The preprocessing steps include:
  1. Remove emojis  
    - select non-emoji text to create new text data
  3. Make all text lower case  
    - Apply .lower() to all text
  5. Remove special characters  
    - Uses regex substitutes 
      - '' for @mentions
      - '' for # hashtag symbol
      - '' for hyperlinks (https://...)
      - ' ' for numbers
      - ' ' for punctuation in string.punctuation
  7. Lemmatization and stemming 
      - Helped reduce overall word count and simplified some common tokens
  9. Remove stop words  
    - Included NLTK's stopwords.words('english') and Sci-kit Learn's ENGLISH_STOP_WORDS  
    - Added:
      - 'bitcoin', 'ethereum', 'binance', 'tether', 'solana'
  10. Tokenize  
      - Used CountVectorizer and TfidfVectorizer from Sci-Kit Learn
      - max_df = 0.7 (no words kept if in >70% of documents)
      - min_df = 3 (words must be in at least 3 documents)
  
*Topic Modeling*  
  
Two different topic models were created and compared: NMF, CorEx. Numerous iterations for each model was undergone in search of decent topic modeling results. The criteria for a successful topic model consisted of clear topics based on if a clear analysis and conlusion can be drawn from the top words. The combination of TfidfVectorizer and NMF was chosen for further manual topic analysis.  
  
  
#### Tools

- [Tweeter API](https://developer.twitter.com/en/docs/twitter-api) for Tweet scrapping
- NLTK, regex, sklearn.feature_extraction.text for text preprocessing
- Pandas for data ingestion and basic exploration
- sklearn.decomposition and corextopic for topic modeling
- Plotly for data visualization


#### Conclusions  
  
I was happy about what I discovered from the tweets considering this is my first NLP project. I was able to find people do have different opinions towards different cryptos, and even some cryptos are based on the same Ethereum blockchain, they have various focuses. Besides, the leadership of the company will affect people's conception towards the token as well. However, with the complexity of crypto and tweets being so sporadic, I didn't get the time to further explore the geographic part of the data, or build a classification model. 
  
In the future, I would like to build machine learning models on this data set and build more interactive visualizaiton, if I ever want to analyze tweets data again. :) 

