---

# 📺 Netflix Content Recommendation System

A content-based recommender system built using natural language processing and unsupervised learning techniques, tailored to Netflix-like data. This project focuses on clustering and similarity modeling to deliver meaningful recommendations, especially for international and regional content.

(<img width="517" height="459" alt="Screenshot 2025-08-05 010817" src="https://github.com/user-attachments/assets/68c282f0-6e92-49c1-ba25-b92d7832944f" />)

---

## 🚀 Project Overview

This project tackles the end-to-end pipeline of building a robust recommendation system using real-world content metadata, The process includes:

* ✅ Data Cleaning & Preprocessing
* 📊 Hypothesis Testing & Statistical Analysis
* 🧠 Feature Engineering using NLP (POS tagging, content synthesis)
* 🤖 Dimensionality Reduction with UMAP
* 🧪 Clustering using HDBSCAN (after KMeans & DBSCAN failed)
* 🔍 Content-Based Recommendations using TF-IDF & Cosine Similarity

---

## 🧠 Why HDBSCAN?

Clustering was a critical challenge. KMeans and DBSCAN both yielded poor silhouette scores and ineffective groupings, After experimenting, **HDBSCAN combined with UMAP** showed significant improvement with a silhouette score of **0.65**, providing more meaningful and tight clusters.

---

## 🛠 Tools Used

* Python 🐍
* Pandas, NumPy
* Scikit-learn
* HDBSCAN
* UMAP
* Matplotlib, Seaborn
* Yellowbrick
* NLTK / SpaCy (for text preprocessing)

---

## 🔍 How It Works

* The `content_detail` field is synthesized using multiple metadata fields (title, description, genre, etc.).
* TF-IDF vectorization transforms this into numerical vectors.
* Cosine similarity computes the closeness between titles.
* A recommendation function filters similar items **within the same cluster** for relevance.



---

## 🧪 Future Improvements

* Add genre-based filters and user profiling
* Deploy as a Flask or Streamlit web app
* Integrate collaborative filtering for hybrid recommendations

---
