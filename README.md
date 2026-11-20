High level description

# Problem name
Financial tweet sentiment with Naive Bayes

## Problem description
The project measures how well Naive Bayes labels short English financial posts as bearish, bullish, or neutral using the Twitter Financial News Sentiment dataset vs just always guessing neutral as a reference.

## Area of AI
Machine learning, supervised text classification

## Applied algorithms
The project trained Multinomial Naive Bayes with two settings and scored both on the same development posts.

- **Single words** counts `missed` and `earnings` separately. It scored **0.673 macro F1**.
- **Single words and pairs** also counts `missed earnings` as a pair. It scored **0.677 macro F1**.

Words and pairs scored higher, so the final test uses that setting.

## Results
On 2,345 validation posts after cleaning and removing texts also present in training, Naive Bayes scored 0.706 macro F1 and the baseline scored 0.264. Naive Bayes found 145 of 338 bearish posts.

## Code location
The comparison runs in financial_tweet_sentiment.ipynb. Sections 2 to 4 select the word counts, fit the classifier and baseline, and compare their results.
