___
Yishu Dai
###  Understand Cryptocurrency Project Proposal 
#### January 9th, 2021
___
  

#### Question/need:
* What is the framing question of your analysis, or the purpose of the model/system you plan to build?   
  
This project will extract text data extracted from Twitter about the top 5 cryptocurrencies to explore who is talking about cryptocurrencies and what aspects they are interested. The purpose of the model I am going to build is to provide some insights into potential cryptocurrency customers for cryptocurrency trading companies to make better marketing strategies.

  
* Who benefits from exploring this question or building this model/system?  
  
  I will personally benefit from this project by getting a deeper understanding of crypto community. Besides, the findings of the project can offer crypto companies insights of social media marketing strategies.   
  
#### Data Description:
* What dataset(s) do you plan to use, and how will you obtain the data?  
  
  The data is going to be text data extracted from Twitter. I will use [Twitter API](https://developer.twitter.com/en/docs/twitter-api) to extract the text data and uses vectorizing, tokenizing, and text preprocessing techniques to clean the data. The initial goal is to do text modeling on the data and hopefully find different types of crypto fans like academics, investors, and speculators.

  
* What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?  
  
  An individual sample will be a single tweet. The features will be tokenized words, n-grams, and potentially other engineered features from techniques such as feature extraction. 
    
  
#### Tools:
* How do you intend to meet the tools requirement of the project?  
 
  I will be using Twitter API to pull the data. NLTK and scikit-learn will be used for text processing. For topic modeling, I will be use NMF and CorEx.  

#### MVP Goal:
* What would a [minimum viable product (MVP)](./mvp.md) look like for this project?  
  
  The goal for the MVP of my project would be to have my dataset downloaded and a text preprocessing pipeline established
  
