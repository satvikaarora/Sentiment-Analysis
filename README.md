# Sentiment-Analysis
Twitter Sentiment Analysis using Tweepy & VADER

This project performs real-time sentiment analysis on tweets fetched from Twitter using the Tweepy API and the VADER Sentiment Analyzer. It helps identify whether public sentiment toward a topic, brand, or individual is positive, negative, or neutral, based on live tweet data.

**Project Overview**

The goal of this project is to analyze Twitter users’ opinions on a given topic or personality using Natural Language Processing (NLP) techniques. The system connects to Twitter’s API using a Bearer Token, fetches recent tweets based on a user-defined query, cleans the text, and evaluates the sentiment of each tweet using VADER (Valence Aware Dictionary and sEntiment Reasoner).

**Key Features**

Twitter API Integration: Fetches live tweets using the Tweepy Client and Bearer Token authentication.

Tweet Cleaning: Removes mentions, URLs, emojis, and special characters using regex.

Sentiment Classification: Uses VADER’s compound score to classify tweets as positive, negative, or neutral.

Rate Limit Handling: Implements retry logic with exponential backoff for safe API usage.

Sentiment Summary: Displays percentage distribution of sentiments and prints sample tweets for each category.

Tech Stack
Component	Description
Language	Python 3.x
Libraries	tweepy, vaderSentiment, re, time
API	Twitter API v2 (Bearer Token Authentication)

**How It Works**

Authentication:
The TwitterClient class initializes a Tweepy Client using your Bearer Token.

Data Retrieval:
The get_tweets() function fetches tweets matching a search query (e.g., "Narendra Modi").

Data Cleaning:
The clean_tweet() method removes user mentions (@username), special characters, and URLs to retain meaningful text.

Sentiment Analysis:
The get_tweet_sentiment() method uses VADER SentimentIntensityAnalyzer to calculate sentiment scores and classify each tweet:

Compound ≥ 0.05 → Positive

Compound ≤ -0.05 → Negative

Otherwise → Neutral

Output Summary:
The program prints the proportion of positive, negative, and neutral tweets, along with sample outputs from each category.
