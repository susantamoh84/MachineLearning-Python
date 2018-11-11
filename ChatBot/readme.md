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

