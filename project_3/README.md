### Overview

Sneakers are a global obsession. Sneaker culture has transcended from the realm of athleticism and is now a stable in the sectors of sportswear, street style, and runway/catway fashion. The global sneaker market was valued at $79 billion in 2020, and that market value is set to increase to $120 billion by 2026. This increase is mostly due to the increasing trend in athleisure, where sneakers are actually now accepted as a business casual item. Sneakers are now even acceptable in the workplace. Coveted sneakers have been seen on everyone from Silicon Valley tech CEOs to actors to famous athletes. ([*source*](https://theconversation.com/the-history-of-sneakers-from-commodity-to-cultural-icon-127268)). 

---

### Problem Statement

As a sneaker store owner, I need to know what people are saying within the sneaker community. I always need to buy new product, and it would be a good business strategy to stock up on products I know are popular and people will buy. Additionally, new sneakers are always coming out and I need to be up-to-date on all the new models and releases. Lastly, knowing what people think about sneakers is important. I can make proper recommendations and address people's concerns based on the opinions I know about the sneaker to help them with their purchase. I want a program that can find reddit data and tell me where it is from. This will be a huge help in determining opinions on various sneakers. 

---

### Datasets

* [`newbalance.csv`](datasets/newbalance.csv): new balance subreddit posts  
* [`nike.csv`](/datasets/nike.csv): nike subreddit posts 
* [`shoes_data.csv`](/datasets/shoes_data.csv): dataset with new balance and nike subreddit data combined  

---

### Data Dictionary
title_token            object
title_tokens_merged    object
subreddit              object
|Feature|Type|Description|
|---|---|---|
|title_token|Object|The title of the subreddit post|
|title_tokens_merged|Object|The words in the title of the post merged after tokenizing, lemmatizing, and stemming the title|
|subreddit|Object|Identifies the subreddit the data came from|

---

### Analysis

Sentiment analysis revealed the positive and negative posts. Positive posts were typically about being happy with a sneaker purchase, enjoying the comfort of their sneakers, or finally getting a pair of sneakers delivered. Negative posts usually dealt with not winning a sneaker raffle, staining their sneakers, or complaining about price. There were some limitations to this analysis, as some positive comments were analyzed as negative, and vice versa. Additionally, an analysis was done using the count vectorizer as the transformer of the data and multinomial naive bayes classifier as the evaluator. The model predicted 0.84 of the data correctly. An analysis was done using the tfidf vectorizer as the transformer of the data and multinomial naive bayes classifier as the evaluator. The model predicted 0.84 of the data correctly. An analysis was done using the count vectorizer as the transformer of the data and the ada boost classifier as the evaluator. The model predicted 0.78 of the data correctly. An analysis was done using the count vectorizer as the transformer of the data and the random forest classifier as the evaluator. The model predicted 0.71 of the data correctly. The models that predicted very well on the train data performed worse on the test data, suggesting the models were overfitted. 

---

### Conclusions/Recommendations 

The analysis using the count vectorizer as the transformer and the multinomial naive bayes classifier performed the best, and was an okay predictor of finding which dataset the data belonged to. I would conduct further analysis using a larger dataset and with more variables. I would also consider the selftext data, if I have a way to analyze pictures, and comments of the submitted posts on those subreddits. 