# Fake News Detection with Multinomial Naive Bayes and K-Nearest Neighbors on Twitter focused on COVID in Brazil

# Project goals
- Extract tweets in portuguese related to the COVID-19 pandemic for further inspection
- Use a pre-determined dataset for training both algorithms
- Clean the training dataset 
- Prepare a model for the dataset in each of the algorithms
- Use the prepared model to inspect the previously extracted tweets
- Determine accuracy and precision on both for research comparisons

# Dependencies
- SciKit Learn
- Numpy
- Pandas
- Seaborn
- NLTK
- Tweepy

# How to run
1. 
It is essential to have access to the Twitter API to execute this. In [tweets_retrieval](tweets_retrieval), we have set all the code for retrieval and you should create a txt file with all the necessary keys, in order:
``` 
    consumer_key
    consumer_secret
    access_token
    access_secret
    bearer_token
```
2. 
Run real_tweets.ipynb, to retrieve live tweets about the Covid context. To change the language retrieved, change the 'pt' to the corresponding BCP 47 language identifier on this line. 

```
    if json_response['data']['lang'] != 'pt':
```

See more information about the twet Lang Operator [here](https://developer.twitter.com/en/docs/twitter-api/enterprise/powertrack-api/guides/operators)

You can also change the [context annotation](https://developer.twitter.com/en/docs/twitter-api/annotations/overview) of the tweets query, to retrieve tweets from others subjects.

3. 
You can stop executing (CTRL + C on the terminal executing the script) once you have enough tweets.

Before you execute fake_news_MNB.ipnyb, you need to run
```
    pip install pandas && pip install numpy
```

after that, before you can use the Tweepy object, you need to create an auth object, like that:

```
    auth = tweepy.OAuthHandler(your_consumer_key, your_consumer_secret)
    auth.set_access_token(you_access_token, your_access_secret)
```

4. 
With this, the setup process is finished and you can execute the MNB and the KNN files to see and compare the results of the algorithms. 


It is also important to declare that the training dataframe was only arranged in the MNB algorithm file. In KNN, we used the final CSV with all of our necessary data.

# About the project

This project was built for our graduation thesis at the University Graduate Program of Computer Engineering - UniCEUB

The reasearch was labeled "Fake News Detection on Twitter using Artificial Intelligence: a comparison between the Multinomial Naive Bayes and K-Nearest Neighbors Algorithms". 

This work has been developed and published by:

- [Bruno Gois – @brunovgois](https://github.com/brunovgois)
- [Matheus Nascimento – @coadordecoffee](https://github.com/coadordecoffee)
