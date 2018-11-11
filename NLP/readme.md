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
  
# TF-IDF
  - Term frequency - inverse document frequency
  - Determine most important words in document
  - Each document may have shared words beyond stop words
  - These words are down-weighted in importance
  - Examples from astronomy: Sky
  - Ensures most common words don't show up as keywords
  - Keeps document specific frequent words high
  - w(i,j) = tf(i,j)*log(N/dfi)
      - w(i,j) = tf-idf weight for token i in document j
      - tf(i,j) = number of occurences of token i in document j
      - dfi = number of documents that contain token i
      - N = total number of documents
    - You want to calculate the tf-idf weight for the word "computer", which appears five times in a document containing 100 words. Given a corpus containing 200 documents, with 20 documents mentioning the word "computer", tf-idf can be calculated by multiplying term frequency with inverse document frequency.
    - Term frequency = percentage share of the word compared to all tokens in the document Inverse document frequency = logarithm of the total number of documents in a corpora divided by the number of documents containing the term
    - Tf-Idf : (5 / 100) * log(200 / 20)

# Named Entity Recognition

  - NLP task to identify important named-entities in the text
    - People, places, organization
    - Dates, states, works of art
    - ... and other categories
  - Can be used alongside topic identification
    - ... or on its own
  - who?, what?, when?, where ?
  
# NLTK and Stanford CoreNLP library

  - The Stanford CoreNLP library
    - Integrates via python via nltk
    - Java Based
    - Support for NER as well as coreferences and dependency trees
    
