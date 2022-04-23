# @elonmusk Tweet Generator 
![alt-text](https://github.com/Siqi-Fang/tweet_generator/blob/main/preview.png)
## Overview

In this project we tuned a pre-trained [GPT-2](https://openai.com/blog/better-language-models/) 124M Model on Elon Musk's tweets from 2010 to 2021. The tuned model can generate a tweet starting with a given prompt or a random tweet with no prompt. 

Sample Output
---
[Prompts] are indicated by brackets.

`Tesla car dealers in America are trying to stop Tesla. Would appreciate your help in fighting for what's right`

`Only, I'm not an investor. Just believe in putting money into my own companies. Don't think the OPM approach is right.`

`Not on the actual moon`

`[I can't believe] there is a real Pied Piper.`

`[Working on] launching @NASA astronauts to the International Space Station next year!`

`[I don't think] Apple is doomed. Just won't unseat Google from 1st place with Larry P in charge.`

## APP Preview 

Data
---
We tuned our model on Elon Musk's 2010-2021 Tweets. The dataset is downloaded from [Kaggle](https://www.kaggle.com/datasets/andradaolteanu/all-elon-musks-tweets). 

The preprocessing include removing entries that are retweets and replies, remove urls, formatting special characters and excluded cleaned tweets with length <= 15 characters. The final training data include 4039 tweets.

Removing retweets and replies has resulted in the most significant improvment in the model's output(evaluated with human inspection). 

For details on preprocessing, visit this [notebook](https://colab.research.google.com/drive/1lBzKme2tkcFL2Inx8c2mM18MM6KHHcVU?usp=sharing).


Advanced Features & Improvements
----
The dataset contained x2 more retweets&reply than original tweets, and we should be using them. We cam tune the model to reply to a tweet that user gives it. 

We can also filter tweets by categories and demographic information and tune a GPT-2 model on them to create a virtual twitter user with desired characteristics.

Depending on how powerful the model is to learn with small amount of training data, we can give it a username and tune a model in real-time. Then have the model generate tweets base on the user's recent activities.


References
---
Max Woolf-- How To Make Custom AI-Generated Text With GPT-2 [tutorial](https://minimaxir.com/2019/09/howto-gpt2/)

HuggingTweets - Train a Model to Generate Tweets [article](https://wandb.ai/wandb/huggingtweets/reports/HuggingTweets-Train-a-Model-to-Generate-Tweets--VmlldzoxMTY5MjI)
