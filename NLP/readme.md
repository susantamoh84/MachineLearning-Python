# NLP

# Overview

  - Fields of study focused on making sense of language
    - Using statistics and computers
  - Basics of NLP
    - Topic identification
    - Text classification
  - NLP applications
    - Chatbots
    - Translation
    - Sentiment Analysis
    - ...more

# Why tokenize

  - Easier to map part of speech
  - Matching common words
  - Removing unwanted tokens

# NLTK Tokenizers

  - sent_tokenize: tokenzie a document into sentences
  - regexp_tokenize: tokenzie a string or document based on regular expression pattern
  - TweetTokenizer: special class just for tweet tokenization, allowing you to separate hashtags, mentions and lots of exclamation points !!!
  
# Bag Of Words

  - preprocessing
    - Helps make for better input data: For Machine Learning & other statistical models
    - Examples:
      - Tokenization for Bag of Words
      - Lower casing of the words
    - Lemmatization/Stemming:
      - Shorten words to their root stems
    - Remove stop words, punctuations or unwanted tokens 

# Gensim
  - Popular open-source NLP library
  - Uses top academic models to perform complex tasks
  - Building document or word vectors
  - Performing topic identification and document comparison
  - Gensim Example: http://tlfvincent.github.io/2015/10/23/presidential-speech-topics/
  
