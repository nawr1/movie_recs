# Movie Recommendation System

## Description

This project is a movie recommendation system built using the MovieLens dataset (25M ratings).
It combines content-based filtering (TF-IDF) and collaborative filtering to suggest movies similar to a given title.

---

## Objectives

* Search for movies using approximate title matching
* Recommend similar movies based on user preferences
* Combine text similarity and user behavior for better recommendations

---

## Dataset

The dataset used is from MovieLens:

https://files.grouplens.org/datasets/movielens/ml-25m.zip

It includes:

* `movies.csv`: movie titles and genres
* `ratings.csv`: user ratings

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* TF-IDF Vectorizer
* Cosine Similarity
* Jupyter Notebook
* ipywidgets

---

## How It Works

### 1. Data Cleaning

Movie titles are cleaned using regex:

* Remove special characters
* Normalize text

### 2. Content-Based Filtering

* TF-IDF is applied on movie titles
* Uses unigrams and bigrams
* Cosine similarity finds similar titles

### 3. Collaborative Filtering

* Identify users who rated a movie greater than or equal to 4
* Extract movies liked by those users
* Compare with global user preferences
* Compute a recommendation score:

Score = (similar users preference) / (all users preference)

### 4. Interactive Search

* Users type a movie title
* The system returns matching titles and recommendations

---

## Installation

```bash
git clone https://github.com/your-username/movie-recommender.git
cd movie-recommender
pip install pandas numpy scikit-learn ipywidgets
```

---

## Usage

1. Download the dataset
2. Place `movies.csv` and `ratings.csv` in the project folder
3. Run the notebook:

```bash
jupyter notebook
```

4. Enter a movie title in the input field to get recommendations

---

## Example

Input:

```
Toy Story
```

Output:

* Toy Story 2 (1999)
* Toy Story 3 (2010)
* Mulan (1998)
* The Iron Giant (1999)
* Mary Poppins (1964)

---

## Key Features

* Fast movie search using TF-IDF
* Personalized recommendations
* Works with large datasets (25M ratings)
* Interactive interface using ipywidgets

---

## Author

Nour Tadili
AI and Data Science Student – ENSAM Casablanca

---

## Future Improvements

* Add deep learning models
* Improve recommendation ranking
* Build a web interface (React and Django)
* Use movie descriptions instead of only titles
