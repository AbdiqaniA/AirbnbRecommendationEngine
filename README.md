# AirbnbRecommend Tokyo
**A Recommender System for Tokyo Airbnb listings leveraging Sentiment Analysis and Collaborative Filtering**

## Motivation
The aim is to develop a Recommender System using publicly available Airbnb data for Tokyo, with the intent to match users with Airbnb listings that align with their preferences.

## Approach
The solution is divided into three segments:

1. **User Preference Identification through Sentiment Analysis**
   - Undertake text preprocessing of each reviewer's comments, including language detection.
   - Employ NLTK's Vader lexicon to determine the compound polarity score for each comment.

2. **Visualization Dashboard**
   - With the computed polarity scores, create a Streamlit dashboard app to visually represent the data.
   - Deploy the application on Heroku for public accessibility.

3. **Recommendation Engine via Collaborative Filtering**
   - Construct a utility matrix with `reviewer_id` on one axis and `listing_id` on the other, incorporating the polarity scores.
   - Apply Singular Value Decomposition (SVD) to predict all missing polarity scores.
   - Generate personalized listing recommendations for users, prioritized by their predicted polarity scores.

## Repository Contents
- `data/`: Contains the `reviews.csv` and `listings.csv` files for Tokyo.
- `Tokyo__SentimentAnalysis.ipynb`: Sentiment analysis processes and computations.
- `Tokyo_Airbnb_Collab.ipynb`: Implementation of the collaborative filtering mechanism and recommendation system logic.

