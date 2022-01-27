Yishu Dai
### Music Tweets NLP Project MVP
#### January 16th, 2022
___

#### MVP
  
Cryptocurrency has gained tremendous popularity in the past few years. With more crypto tokens and NFTs popping up, I started wondering what are people talking about cryptos in social media? Twitter, Discord and Telegram are the most common tools used by crypto community, since the latter two are not public plarforms, I decided to look into tweets that inlclude text or hashtags of the top 5 cryptocurrencies. I hope to get a better understanding of people's thoughts and interests in crypto and provide some insights to my new job (a blockchain company)

For this project, I downloaded 10,000 tweets using [Twitter API](https://developer.twitter.com/en/docs/twitter-api). The keywords are: bitcoin, ethereum, binance, tether and solana. 

The pipeline processess in the following order:

  1. Remove Emojis
  2. Make all text lowercase
  3. Remove mentions, hashtags, punctuation, numbers, hyperlinks
  4. Remove non-english words
  5. Remove tweets if empty due to character removal
  6. Remove duplicate cleaned tweets
  7. Lammetization.

The modeling process is separate for each crypto. With some tuning of min_df and max_df, I create 10 basic topics for bitcoin using NMF model. The boundries of the 10 topics are ambiguous as there are not specific genres when it comes to crypto investment.

#### Further Work  
The next step is to get samples of each topic to figure out what each topic is about. And if I can find significant differences between the topics, I would do some work with clustering to get more information about the data. 
