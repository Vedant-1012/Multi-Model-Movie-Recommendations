# A Multi-Model Approach to Personalized Movie Recommendations

This project explores and implements multiple recommendation models, including **Logistic Regression**, **Bayesian Personalized Ranking (BPR)**, and **Hybrid Neural Collaborative Filtering (NCF)**, to provide personalized movie recommendations. The goal is to compare and contrast the performance of these models in predicting user preferences.

---

Dataset : https://drive.google.com/drive/folders/1vLFjzhXY6JxetgsWz6kFCBKW9VvXMWwM?usp=sharing

## Table of Contents
1. [Abstract](#abstract)
2. [Methodology](#methodology)
3. [Results](#results)
4. [How to Run the Code](#how-to-run-the-code)
5. [Dataset](#dataset)
6. [Dependencies](#dependencies)
7. [References](#references)

---

## Abstract
Movie recommendation systems are crucial for predicting and recommending movies that users are likely to enjoy. This project implements and evaluates three key models:
1. **Logistic Regression**: A content-based model using TF-IDF for text features.
2. **Bayesian Personalized Ranking (BPR)**: A ranking model optimized using LightFM.
3. **Hybrid Neural Collaborative Filtering (NCF)**: A deep learning model combining collaborative filtering with metadata features.

The models are evaluated using metrics such as **NDCG**, **Precision**, **Recall**, **RMSE**, and **MAE**.

---

## Methodology
### 1. Logistic Regression
- Preprocessed movie descriptions and genres using TF-IDF.
- Trained a binary classification model to predict whether a user will like a movie.
- Evaluated using Precision, Recall, ROC-AUC, and NDCG.

### 2. Bayesian Personalized Ranking (BPR)
- Used the LightFM library to implement BPR.
- Created implicit data from user ratings (≥3.5 = liked, <3.5 = not liked).
- Evaluated using Precision, Recall, and NDCG.

### 3. Hybrid Neural Collaborative Filtering (NCF)
- Combined user-item interactions with metadata features (e.g., genre, budget, runtime).
- Built a neural network model using TensorFlow/Keras.
- Evaluated using RMSE, MAE, Precision, Recall, and NDCG.

---

## Results
- **Logistic Regression**: NDCG@10 = 0.7281, Precision = 0.7017
- **BPR**: NDCG@10 = 0.9440, Precision = 0.9124
- **Hybrid NCF**: NDCG@10 = 0.7597, RMSE = 0.2024

For detailed results, check out the [results folder](./results/).

---

## How to Run the Code
1. Clone the repository:
   ```bash
   git clone https://github.com/Vedant-1012/Multi-Model-Movie-Recommendations.git
