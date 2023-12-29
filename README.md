# Movie Sentiment Analysis with DistilBERT

🎬 Analyzing sentiments in movie reviews using DistilBERT and VADER sentiment analysis.

## Overview

This project analyzes sentiments in Imdb "Barbie 2023" movie reviews using a combination of web scraping, sentiment detection, and machine learning. The process involves web scraping reviews, applying VADER sentiment analysis, and fine-tuning a DistilBERT model on a Kaggle IMDb dataset.

## Features

- **Web Scraping:** Gathered diverse user reviews using Selenium.
- **Sentiment Analysis:** Utilized the VaderSentiment library to perform sentiment analysis on user reviews scraped from the Barbie 2023 movie. The primary goal was to gain insights into the sentiment expressed by users and compare it with the ratings they provided for the movie.

The purpose of incorporating sentiment analysis was two-fold:

1. ***Detecting Discrepancies:*** Often, users may express sentiments in their reviews that are not entirely aligned with the numeric ratings they give. VaderSentiment helped identify instances where users may have given a positive rating but expressed negative sentiments or vice versa. Recognizing such discrepancies is crucial for understanding the true sentiments associated with the movie.

2. ***Enhancing Model Training:*** The results of the sentiment analysis were used to preprocess the data before applying fine-tunined NLP DistilBERT classification model for sentiment analysis. By filtering out instances with conflicting sentiments and ratings, the model predictions became more reliable.

- **Data Cleaning:** Filtered conflicting sentiments for improved accuracy.
- **DistilBERT Model:** Fine-tuned for sentiment analysis on Kaggle IMDb dataset.
- **Results:** Enhanced sentiment predictions for movie reviews.


### Prerequisites

- Python 3.9.x
- ChromeDriver 119.0.6045.105
- vaderSentiment
- Transformers
- Torch

## Dataset

The dataset "Imdb 50K" used in this project can be found [here](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/).


**WARNING:** I recommend using a machine with a good GPU when fine-tuning a transformer model ☹. I used available acceleration GPU P100 on kaggle.

