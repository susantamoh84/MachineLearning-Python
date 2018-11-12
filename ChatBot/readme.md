# Building ChatBot

  - Implement smalltalk, Eliza style
  - Use regex and ML to extract meaning from free-flow text
  - Build ChatBot that can
    - Query a database
    - Plan a trip
    - Help you order coffee
  - Handling Statefulness

# Why Personality?

  - Difference between command line app and chatbot
  - Makes chatbots and voice assistants more accessible and fun to use
  - Your users will expect it

# NLU - Natural Language Understanding

  - "I am looking for a mexican restaurant in the center of the town" -> NLU -> {Intent: restaurant_search, entities:{cuisine:mexican,area:center}} -> Database -> Response

# Intents
  - restaurant_search:
    - I am hungry
    - Show me good pizza spots
    - I want to take my boyfriend out for sushi

# Entities
  - NER - Named Entity Recognition

# Using Regular Expression for Intents & NER
  - Simpler than ML models
  - Computationally efficient
  - Drawbacks:
    - Debugging regular expressions can be difficult

# Word Vectors
  - Context: 
    - Lets meet at the _ tomorrow. Candidates: office, gym, park, beach, party
    - I love going to the _ to play with the dogs. Candidates: beach, park
  - Word Vectors try to represent meaning of words
  - Words which appear in similar context appear to have similar vectors
  - Words vectors training is computationally intensive and requires a lot of data.
  - Available word vectors: Glove Algorithm, similar to word2vec
  - Spacy

# Word Vectors Similarity
  - Direction of vectors matters
  - "Distance" between the words = angle between the vectors
  - Cosine Similarity:
    - 1: If vectors point in the same direction
    - 0: if vectors are perpendicular
    - -1: If vectors point in the opposite direction
    
# Intent Supervised Learning
  - A classifier predicts the intent label given a sentence
  - 'Fit' classifier by tuning it on training data
  - Evaluate performance on test data
  - The fraction of labels we predict correctly
  
# Nearest Neighbour Classification
  - Simplest solution - look for the labeled example (training data) that is most similar in (test data)
  - Use its intent as the best guess
  
# Support Vector Machines
  - Nearest beighbour is too simple - need a better solution
  - SVM/SVC - Support Vector Machine/Classifier
  
# Entity Extraction
  - Beyond Keywords: Context ( Keywords don't work for entities you haven;t seen before )
  - Use contextual clues :
    - Spelling
    - Capitalization
    - words occuring before and after
  - Pattern recognition
  
# Dependency Parsing
  - Use a parse tree to assign roles
  - parse tree hirearchial relationship - parent child
  - Example: "A flight from Shanghai to Singapore"
    - The word "to" is parent of word "Singapore"
    - The word "from" is parent of word "Shanghai"
    
# Virtual Assistants
  - Common chatbot use cases:
    - Scheduling a meeting
    - Booking a flight
    - Searching for a restaurant
  - Require information about the outside world
  - Need to interact with databases or APIs

# Incremental slot filling and negation
  - Add responses into the memory
  - When to wipe memory of bot
  - Negation:
    - Where should i go for dinner ?   "what about Sally's Sushi Place ?"
    - no I don't like sushi            "ok, what about Joe's Steakhouse ?"
    - Specific to the application context
  - Negated Entities
    - assume that "not" or "n't" just before an entity means user wants to exclude this
