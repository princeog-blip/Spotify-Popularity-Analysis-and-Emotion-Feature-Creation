# Spotify-Popularity-Analysis-and-Emotion-Feature-Creation

## Overview
This code uses a spotify dataset to engineer a new feature representing the emotion a song displays. It also analyzes what makes a song popular using features within the dataset and the new emotion feature.

## Dataset
The dataset was obtained through Kaggle.com and can be accessed with the following link: https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset#

## Methods Used
1. Feature Egineering using valence and energy (emotion feature created)
2. Feature Egineering using K-Means Clustering (emotion_kmeans feature created)
3. Random Forest Classifier
4. Support Vector Machine
5. Linear Regression
6. Lasso Regression
7. Gradient Boosting Regression
8. Logistic Regression

## Key Findings
The data-driven approach of K-Means clustering to create the emotion feature performed slightly worse than the theory driven approach of using a predefined threshold of valence and energy (previous research proves this method) when classifing emotion with Random Forest and SVM. 

Popularity is extremly hard to predict with the given dataset. The numerical audio features tested with Linear, Lasso, and Gradient Boosting Regression all had very low R-squared values indicating poor performance with predicting popularity. Logistic Regression appread to work well at first with the categorical features, but after further analysis, it was found the classes are actually very imbalanced and Logictic Regression only predicted the majority class each time. After Logistic Regression was improved to make sure both classes were predicted track genre was found to be important for predicting popularity, but the low precision score of the popular class means the model is still not performing the best. 

Overall, other outside factors such as marketing or social trends are likely to play an effect on popuarity, but this is not included in this dataset. Only audio features and features engineered from audio features alone are not enough to effectively predict popularity. 

## Files
Attached ipynb contains all code and visuals: 'Spotify_Analysis.ipynb'

## Author
Olivia Prince
