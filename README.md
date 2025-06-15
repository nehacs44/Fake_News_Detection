# Fake News Detection
## Objective
The objective of this assignment is to develop a Semantic Classification model. You will be using Word2Vec method to extract the semantic relations from the text and develop a basic understanding of how to train supervised models to categorise text based on its meaning, rather than just syntax. You will explore how this technique is used in situations where understanding textual meaning plays a critical role in making accurate and efficient decisions.
## Business Objective

The spread of fake news has become a significant challenge in today’s digital world. With the massive volume of news articles published daily, it’s becoming harder to distinguish between credible and misleading information. This creates a need for systems that can automatically classify news articles as true or fake, helping to reduce misinformation and protect public trust.


In this assignment, you will develop a Semantic Classification model that uses the Word2Vec method to detect recurring patterns and themes in news articles. Using supervised learning models, the goal is to build a system that classifies news articles as either fake or true.

 The following are the steps used:
1.	Data Prepration: 
The data consists of two tables True news and fake news. Since it is a classification problem we need to assign labels to each class. True news assigned as news_label:1 and fake news as 0. The final data can be achieved by merging both the data. The data was partially clean except for a few null values. Hence, where Text is having null values those rows can be removed. The insignificant columns (not part of our analysis) can be removed.

2.	Text Preprocessing: 
Text preprocessing is done by lowercasing the text, removing square brackets, remove punctuation, remove words containing numbers followed by POS tagging and lemmatization on the cleaned news text and remove all words not tagged as NN or NNS. And saved the cleaned data as a csv file. 

 3.  Train-Test split: 
The split was done at 70% and 30% for train and test data respectively with stratification to obtain proportional ratio of True and Fake news in train and test data.

 5. EDA: 
EDA performed on cleaned and preprocessed data by visualizing the training data according to the character length of cleaned news text and lemmatized news text with POS tag removed. Top 40 words is obtained by frequency in true news and fake news using word cloud. Unigrams , bigrams and trigrams of both news is compared.
 6. Feature Extraction: 
Converted text into vector form using Word2Vec vectorizer.

 7. Model training and evaluation: 
Model is trained by using Logistic regression , Decision Tree and Random Forest. The result is compared between all the three models and chosen random forest for decision as it has highest accuracy , precision , recall and f1 among all the three models.
LR : Accuracy: 90%    , Precision: 91%    , Recall: 90% ,      F1:90%
DT: Accuracy:82%     , Precision: 82%    , Recall: 85%,      F1: 83%
RF: Accuracy: 91%    , Precision:  91%   , Recall: 92% ,      F1: 91%

8. Conclusion:
1. True news consists of fact based and formal language whereas fact news displayed by emotionally charged,sensational or misleading phrasing.
2. Some of the most frequently words used in fake news as per wordcloud ,unigram, bigram and trigram are attack, fact,question, case,news, image, video, woman, man which are catchy and emotion driven words whereas true news consists more of formal and balanced words like government, administration,country, election, official.
3. Here we can see the model is best described by Random forest with 91% accuracy ,91% precision 92% recall and 91% f1-score.
4. The evaluation matrix chosen for decision is Recall score as we want to predict true news correctly.
