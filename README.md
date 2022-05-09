# Fake News Prediction:

Fake news is one of the biggest issues in the current era of the internet and social media. While it’s a blessing that the news flows from one corner of the world to another in a matter of a few hours, it is also painful to see many people and groups spreading fake news.

Machine Learning techniques using Natural Language Processing and Deep Learning can be used to tackle this problem to some extent. I have built a Fake News Detection model using Natural Language Processing.

## Data and Problem:

I have used Kaggle Fake News Challenge Data to make a classifier. The dataset consists of 4 features and 1 binary target. The 4 features are as follows:

id: unique id for a news article

title: the title of a news article

author: author of the news article

text: the text of the article; could be incomplete

label: a label that marks the article as potentially unreliable

1: Fake

0: Real

## Data Preprocessing and Cleaning:

First, I removed the missing values with empty string ' ', I merged the Author and title in a new column named content.

After seprating the data and labels, I did the following steps:

- Removing stop words: There are a lot of words that add no value to any text no matter the data. For example, “I”, “a”, “am”, etc. These words have no informational value and hence can be removed to reduce the size of our corpus so that we can focus only on words/tokens that are of actual value.

- stemming the words: Stemming is the techniques to reduce the words to their stems or roots. The main advantage of this step is to reduce the size of the vocabulary. For example, words like Acting, Actor, Actress will be reduced to “Play”. Stemming just truncates the words to the shortest word and doesn’t take into consideration the grammatical aspect of the text. 

- Removing everything apart from alphabetical values: Non-alphabetical values are not much useful here so they can be removed.

- Lower case the words: Lower case the words to reduce vocabulary.

## Converting the textual data into numerical data:

We need to convert textual data into numerical because Maching learning algorithm can't be applied to  text data. I have used TF-IDF Vectorizer for this purpose.

### TF-IDF Vectorizer

Now we need to vectorize the words to numerical data which is also called vectorization. The easiest way to vectorize is to use the Bag of Words. But Bag of Words creates a sparse matrix and hence there is a lot of processing memory needed. 

### Spliting the data into training and test data

### Modelling: Logistic Regression

I used the Logistic Regression which is the most promising algorithm preferred for classification. I fit on the training data and predict on the test data. Later I calculate and get an accuracy of 98%. 

### Predictive System:
I make a predictive system which predicted successfully whether the news is fake or real.

