
# 🎧 Spotify Song Popularity Prediction

Predicting whether a song will be popular using Spotify audio features and machine learning models.

---

## 📌 Project Overview

This project explores how audio-based features from the Spotify dataset can be used to classify songs as **popular** or **not popular**. A song is considered **popular** if its popularity score is greater than 70 (on a scale of 0–100). We apply data preprocessing, feature engineering, and machine learning techniques to build and evaluate classification models.

---

## 📂 Dataset

- Source: [[Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)]
- Features include:
  - `danceability`
  - `energy`
  - `valence`
  - `tempo`
  - `loudness`
  - `speechiness`
  - `acousticness`
  - `instrumentalness`
  - `duration_ms`
  - `popularity` (target)
  - and more...

---

## 🛠 Feature Engineering

New features were created to better capture musical characteristics:
- **`mood_score`**: Average of `valence` and `energy` to estimate overall track emotion.
- **`dance_potential`**: Product of `danceability` and `energy`.
- **`tempo_category`**: Songs bucketed as Slow, Medium, or Fast based on tempo.
- **`loudness_norm`**: Normalized loudness score for better modeling.

---

## 🤖 Machine Learning Models

We trained and evaluated the following models:
- **Random Forest Classifier**
- **XGBoost Classifier**

Models were tuned using **RandomizedSearchCV**, and performance was measured using:
- Accuracy
- Precision
- Recall
- F1-score

---

## 📈 Results

| Model              | Accuracy | Notes                         |
|-------------------|----------|-------------------------------|
| Random Forest      | ~98%     | Strong baseline               |
| XGBoost Classifier | ~96%     | Best performance overall      |

RandomForest outperformed other models, achieving the highest accuracy and better classification metrics across the board.

---

## 📊 Visualizations

- Correlation matrix to explore feature relationships
- Popularity distribution
- Tempo category vs popularity
- Feature importances (XGBoost)

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/spotify-popularity-prediction.git
   cd spotify-popularity-prediction
