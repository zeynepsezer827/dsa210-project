# DSA210 Term Project

# TikTok-Spotify_Correlation_DSA210_Zeynep_Sezer

DSA210 Term Project / Spring 2025-2026

# DSA210 Project: Analysing the Relationship Between TikTok Popularity and Spotify Streams

## Motivation

Social media platforms have become very important in the music industry, especially TikTok. Many songs become viral through short videos and trends before becoming popular on Spotify or YouTube.

I have always been interested in how social media affects people's music choices and how songs suddenly become popular online. Because of this, I wanted to explore whether TikTok popularity has a measurable relationship with Spotify streaming performance.

The goal of this project is to analyze social media data and test whether machine learning models can predict Spotify streams using TikTok-related metrics.

---

## Overview

This project investigates the relationship between TikTok popularity and Spotify streaming success.

By combining datasets from TikTok, Spotify, YouTube, Instagram, and Snapchat, I analyzed whether engagement metrics such as likes, shares, comments, popularity scores, and views are related to Spotify stream counts.

The project includes:
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Hypothesis testing
- Machine learning models
- Clustering analysis

---

## Data to be Used

### TikTok Dataset

* Source: Kaggle TikTok music trend dataset
* Features:
  - track_name
  - artist_name
  - likes
  - comments
  - shares
  - views
  - release_date

### Spotify & YouTube Dataset

* Source: Kaggle Spotify and YouTube statistics dataset
* Features:
  - Spotify streams
  - popularity score
  - YouTube views
  - artist information

### Instagram & Snapchat Dataset

* Source: Kaggle social media trend dataset
* Features:
  - popularity metrics
  - trend scores
  - song information

---

## Methodology

# Data Cleaning & Integration

* The datasets had different formatting styles for song and artist names.
* I cleaned the text columns by:
  - converting to lowercase
  - removing special characters
  - removing “feat.” and similar text
  - removing text inside parentheses

* Initially, merging only with track names created incorrect matches and noisy data.
* After feedback from the previous milestone, I improved the merge quality by using both track name and artist name together.
* Duplicate rows were also removed before merging.

# Exploratory Data Analysis (EDA)

* I analyzed the distributions of popularity variables.
* Correlation heatmaps and scatterplots were created.
* Relationships between TikTok metrics and Spotify streams were explored visually.

# Hypothesis Testing

I tested whether social media popularity is related to Spotify streaming performance.

### Hypothesis 1
* Null Hypothesis:
TikTok popularity has no relationship with Spotify streams.

* Alternative Hypothesis:
Songs with higher TikTok engagement tend to have higher Spotify streams.

### Result
* Correlation analysis showed a positive relationship between several TikTok metrics and Spotify streams.
* The null hypothesis was rejected for some engagement variables.

---

## Machine Learning (ML)

In the final phase of the project, machine learning methods were applied to predict Spotify streaming performance.

### 1. Linear Regression

* Goal:
Predict Spotify streams using social media metrics.

* Result:
Linear Regression provided a baseline model but had limited performance because the relationships between variables were not fully linear.

---

### 2. Random Forest Regression

* Goal:
Capture more complex relationships between TikTok popularity and Spotify streams.

* Result:
Random Forest performed better than Linear Regression and produced more reliable predictions.

* Feature importance analysis showed that some engagement variables contributed more strongly to prediction performance.

---

### 3. Random Forest Classification

* Goal:
Predict whether a song is a “hit” or not.

* Method:
Songs above the median Spotify stream count were labeled as hits.

* Result:
The model achieved moderate classification accuracy and successfully identified some hit patterns.

---

### 4. K-Means Clustering

* Goal:
Group songs with similar popularity behaviors.

* Method:
The Elbow Method was used to determine the number of clusters.

* Findings:
The clustering analysis identified groups of songs with different engagement and streaming patterns.

---

## Findings

* TikTok engagement metrics showed a measurable relationship with Spotify streams.
* Random Forest Regression performed better than Linear Regression.
* Some social media metrics were more important than others in prediction tasks.
* Songs with higher engagement generally tended to have higher streaming performance.

---

## Limitations & Future Work

* Different datasets used inconsistent formatting for songs and artist names, which made merging difficult.
* Even after improving the merge process, some noisy matches may still remain.
* The datasets were limited in size and did not contain real-time information.

Future improvements could include:
* Using official Spotify or TikTok APIs
* Collecting larger datasets
* Using deep learning models
* Adding sentiment analysis from comments or lyrics

---

## Project Structure

* `proposal.pdf`:
Project proposal document.

* `milestone1.ipynb`:
EDA, cleaning, visualization, and hypothesis testing.

* `milestone2.ipynb`:
Machine learning models and clustering analysis.

* `requirements.txt`:
List of Python dependencies.

* `final_report.pdf`:
Final project report.

---

## Libraries Used

Main Python libraries used in the project:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn


## AI Usage Disclaimer

In this project, AI tools were used for limited coding assistance, debugging during the development process.

All analysis decisions, dataset selection, data cleaning process, and interpretation of results were completed by me.
