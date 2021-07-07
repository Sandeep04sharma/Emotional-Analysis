# Emotional-Analysis
 Emotional Analysis on Twitter dataset


### Steps:

##### 1. Import libraries:
```python
import twitter
import random
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import json
import re
import unicodedata
from wordcloud import WordCloud
import spacy
from spacy.lang.en.stop_words import STOP_WORDS
import nltk
nltk.download('stopwords')
from nltk.corpus import stopwords
#import sklearn
from nltk.stem.porter import PorterStemmer
ps=PorterStemmer()

```
##### 2. Authentication with twitter credential
In order to use twitter api we need to create developer account on twitter
they will provide you keys and token, here is sample keys and thier syntax to use with twitter api in python
**NOTE** Use your own credential, mine will not work on your system.
```python

CONSUMER_KEY = 'Ri9pFOQqXSnHm8p8IZj5QCw16'
CONSUMER_SECRET = 'hRrAioGsLbwWHp0fAmrCNZkbhOd2E3mRYeAB6OUZlQD36y1jej'
OAUTH_TOKEN = '1258017464174219269-y9B2ac2711bcaYEHoSqi3qJ7RXGuMY'
OAUTH_TOKEN_SECRET = 'i8JW4em2QuH0e4H5Ahy9SYn0wXSBDaafDsZJrmweYc79Z'
auth = twitter.OAuth(OAUTH_TOKEN, OAUTH_TOKEN_SECRET,
CONSUMER_KEY, CONSUMER_SECRET)
twitter_api = twitter.Twitter(auth=auth)

```

##### 3. All the preprocessing task
 You can find [data set](https://drive.google.com/file/d/13WPOrRAzSbhxzdJqRkSrUaTPJZdfbuXo/view?usp=sharing) here.
##### 4. Model building
At this phase we used diffrent classifier on our dataset, here is all
1. Stochastic Gradient Descent - 65% accuracy
2. Logistic Regression         - 67%
3. Random Forest Classifier    - 65%
4. Support Vector Classification - 68%
 ##### 5. Result:
 Classification report for SVM:
 
 ![class](https://user-images.githubusercontent.com/54997938/124806773-b031f400-df7a-11eb-904f-d076ada323f5.jpg)

