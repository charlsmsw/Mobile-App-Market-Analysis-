📱 Mobile App Market Analysis

Exploratory data analysis (EDA) of the Google Play Store app dataset — uncovering what drives installs, ratings, and pricing across the mobile app market.

Domain: Sales & E-commerce — Mobile App Market

Problem Statement

The mobile app market is huge and highly competitive, with millions of apps competing for user attention across dozens of categories. This project answers key questions for developers, publishers, and marketers:


Which app categories are most crowded, and which are underserved?
Does app pricing affect installs and ratings?
What separates a highly-rated app from a poorly-rated one?
Which categories drive the most installs, and how do free vs. paid apps compare?


Dataset


File: googleplaystore.csv (not included — see Setup)
Size: 10,841 rows × 13 columns
Fields: App, Category, Rating, Reviews, Size, Installs, Type, Price, Content Rating, Genres, Last Updated, Current Ver, Android Ver


Notebook Structure

mobile_app_market_analysis.ipynb is organized as an end-to-end EDA:


Data Loading and Initial Overview — load the raw CSV and inspect shape, dtypes, and structure
Data Pre-processing — cleaning and feature preparation
Exploratory Data Analysis

3.1 Univariate Analysis
3.2 Bivariate Analysis
3.3 Multivariate Analysis



Key Insights — five decision-relevant findings from the data
Conclusion & Recommendations — actionable takeaways for developers and publishers


Key Findings


Rating is a poor predictor of popularity — the correlation between Rating and installs is weak (well under 0.2).
The market is highly concentrated — FAMILY, GAME, and TOOLS dominate app counts, while categories like BEAUTY, EVENTS, and COMICS are comparatively underserved.
Free apps dominate installs — roughly 92% of apps are free, and paid apps show visibly lower install volumes even within the same category.
Price doesn't hurt ratings — paid apps are rated comparably (sometimes slightly higher) than free apps.
App size is essentially irrelevant to both rating and install count.


Recommendations


Favor a freemium/free-with-IAP model over a flat paid price to maximize install volume.
Avoid over-saturated categories (GAME, FAMILY, TOOLS) unless you have a differentiated product; consider less crowded categories like EVENTS, EDUCATION, or BOOKS_AND_REFERENCE.
Don't over-invest in shrinking app size as a standalone quality lever.
Treat a 4.0+ rating as a floor, not a growth lever — marketing and distribution effort matters more once quality is baseline-acceptable.


Setup


Download the dataset (e.g. from Kaggle: Google Play Store Apps) and save it as googleplaystore.csv in the same directory as the notebook.
Install dependencies:


bash   pip install pandas numpy matplotlib seaborn plotly jupyter


Launch the notebook:


bash   jupyter notebook mobile_app_market_analysis.ipynb

Requirements


Python 3.12+
pandas, numpy
matplotlib, seaborn, plotly


Next Steps


The dataset lacks a genuine revenue/exact-download-count field (installs are bucketed).
A companion Play Store reviews dataset (with review text) could enable sentiment analysis to complement these quantitative findings.
