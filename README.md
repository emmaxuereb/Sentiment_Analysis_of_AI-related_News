# AI News Over Time: A Sentiment Analysis

This project investigates how media sentiment in AI-related news headlines has evolved over time, from January 2022 to May 2024. Using Natural Language Processing techniques and two sentiment analysis models, VADER and RoBERTa, we analyze trends in media tone across time, topics, and countries.

## Project Summary

- Dataset: 23,689 news articles mentioning "AI" or "Artificial Intelligence"
- Filtered to 12,280 AI-relevant articles using cosine similarity with AI-relevant text
- Sentiment models:
  - **VADER**: Rule-based sentiment analysis
  - **RoBERTa** (`cardiffnlp/twitter-roberta-base-sentiment`): Transformer-based sentiment classifier
- Analysis focuses on:
  - Sentiment trends over time
  - Differences in sentiment across five domains (sports, economics, health, politics, education)
  - Sentiment variation by country

## Code Overview

The main steps in the notebook include:

1. **Data Loading & Preprocessing**
   - Remove irrelevant articles using sentence-transformer-based cosine similarity filtering
   - Clean text (remove punctuation, numbers, stopwords, etc.)

2. **Sentiment Analysis**
   - Apply VADER and RoBERTa to compute sentiment scores for article headlines
   - Visualize proportions of positive, neutral, and negative sentiment over time

3. **Topic and Country Filtering**
   - Filter subsets for specific topics using cosine similarity with topic-specific reference texts
   - Map articles to countries based on news outlet

4. **Evaluation**
   - Manual annotation of 96 headlines for model validation
   - Model consistency agreement matrix

5. **Visualization**
   - Time-series plots of sentiment by topic and country
   - Confusion matrices comparing model predictions with human annotations

---

This project was carried out as part of a group assignment for the Applied Data Science Master's program at Utrecht University.
