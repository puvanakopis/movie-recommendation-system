# 🎬 Movie Recommendation System

A content-based movie recommendation system built with **Streamlit** and **TMDB API**.  
It recommends the top 10 similar movies based on a user-selected title and displays their posters.

---

## 📌 Overview

This project uses **TF-IDF vectorization** and **cosine similarity** on movie metadata (genres, keywords, cast, crew, overview) to find movies similar to a given one.  
The web interface is built with **Streamlit**, and movie posters are fetched from **The Movie Database (TMDB) API**.

---

## ✨ Features

- Select any movie from the dataset (TMDB 5000 movies).
- Get top 10 content‑based recommendations.
- View movie posters alongside titles.
- Fast recommendations using pre‑computed similarity matrix.

---

## 🧠 How It Works

1. **Data Preprocessing**  
   - Merges `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`.  
   - Extracts genres, keywords, top 3 cast members, and director.  
   - Combines them into a single `tags` column.

2. **Vectorization & Similarity**  
   - Converts `tags` into TF‑IDF vectors.  
   - Computes cosine similarity between all movies.

3. **Recommendation**  
   - For a given movie, finds the 10 most similar movies by cosine distance.  
   - Retrieves their titles and TMDB IDs.

4. **Posters**  
   - Uses TMDB API (`https://api.themoviedb.org/3/movie/{id}`) to fetch poster images.

---

## 📁 Dataset

- **Source**: [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) from Kaggle.
- Files used:
  - `tmdb_5000_movies.csv`
  - `tmdb_5000_credits.csv`

> **Note**: The dataset is not included in this repository. You must download it from Kaggle and place it in a `data/` folder.

---

## 🛠️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/movie-recommendation-system.git
cd movie-recommendation-system
