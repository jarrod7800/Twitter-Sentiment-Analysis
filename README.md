

# Twitter - Sentiment - Analysis


-- Project Status: 
[complete, need to switch out training dataset and retrain on better data]


### Project Intro/Objective

The purpose of this project is to explore the twitter api, and to fit different classification models onto the data and then predict a tweet's seniment. The labels for sentiment are: Negative, Neutral, and Positive. We will use metrics like f-1 score and ROC graphs to to gauge performance then will show top two performing. 


### Methods Used -

- Natural Language Processing
- Machine Learning


### Technologies -

- Tweepy API
- SciKit Learn
- NLTK
- Numpy
- Python
- Pandas
- Jupyter


### Project Description - 

We begin by using the Tweepy api and configuring the setup to get the relavent data. To do this we set up a TwitterClient object class and create our query. We then quickly clean the tweets and assign a sentiment to them via TextBlob before outputting to a csv. We then use the Sentiment models file to input these tweets from before and use NLTK and basic natural language processing preprocessing before using a tfidf vectorizer with bigram data as our inputs. We then finally begin building our various classification models and thelastly compare each model's performance.

As of right now the project is completed, but honestly the model could perform better perhaps with better data quality. The bitcoin tweets I initially pulled did not have a great distribution of sentiments to begin with. Realizing it may be redundant to train my models on another models predictions I pivoted and began to manually assign sentiment to each tweet (the program automatically uses TextBlob model to assign a base sentiment). This approach is time consuming compared to auto assigning, however I beilieve it may be important initially when training the models. Also due to the nature of bitcoin tweets a decent number of tweets were recurring price update tweets which were hard to filter for intially. Perhaps something either more polarizing or a different dataset altogether to train the model would be better. In the near future I plan on coming back and recreating the models with different data to analyse results. I also intend to add a cross validation section to the sentiment models file.

To run the code for yourself with a query of your choosing, first fork the code and open get tweets for sentiment. Start by changing the api key info to your own api key. I used configparser and created a seperate file to hold my api keys. Enter your query and the number of tweets you would like, edit the file name, and run the code. This will output a csv file of your tweets which you will then run the model on in seniment models. In the sentiment models file you simply need to access the file path for your tweets and then run the code on it.




Relevant Data is being kept ['here']('https://github.com/jarrod7800/Twitter-Sentiment-Analysis/tree/main/Twitter_Sentiment_Analysis/CSVs') within this repo.
