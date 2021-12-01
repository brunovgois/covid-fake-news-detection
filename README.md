# Fake News Detection with Multinomial Naive Bayes and K-Nearest Neighbors on Twitter focused on COVID in Brazil

# Project goals
- Extract tweets in portuguese related to the COVID-19 pandemic for further inspection
- Use a pre-determined dataset for training both algorithms
- Clean the training dataset 
- Prepare a model for the dataset in each of the algorithms
- Use the prepared model to inspect the previously extracted tweets
- Determine accuracy and precision on both for research comparisons

# Tech
We have selected a few libraries to work on the project. We used:
- SciKit Learn
- Numpy
- Pandas
- Seaborn
- NLTK
- Tweepy

# Observations

It is essential to have access to the Twitter API to execute this. In ["tweets_retrieval"](tweets_retrieval), we have set all the code for retrieval and you should create a txt file with all the necessary keys, as follows:
```
with open('keys.txt', 'r') as tfile:
    consumer_key = tfile.readline().strip('\n')
    consumer_secret = tfile.readline().strip('\n')
    access_token = tfile.readline().strip('\n')
    access_secret = tfile.readline().strip('\n')
    bearer_token = tfile.readline().strip('\n')
```

It is also important to declare that the training algorithm was only arranged in the MNB algorithm file. In KNN, we used the final CSV with all of our necessary data.

# About the team and project

This project was built for our final thesis in the University Graduate Program of Computer Engineering at UniCEUB, Brasília, Brazil, 2º/2021.

The reasearch was labeled "Fake News Detection on Twitter using Artificial Intelligence: a comparison between the Multinomial Naive Bayes and K-Nearest Neighbors Algorithms". 

This work has been developed and published by:

[Bruno Gois – @brunovgois](https://github.com/brunovgois)

[Matheus Nascimento – @coadordecoffee](https://github.com/coadordecoffee)
