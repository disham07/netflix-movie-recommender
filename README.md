# 🎬 Netflix Movie Recommender System

A content-based movie recommendation system built using Python, Pandas, and Scikit-learn. The project recommends movies similar to a user's selected title by analyzing movie genres and descriptions.

## 📌 Project Overview

Finding movies to watch can be difficult when there are many options available. This project helps users discover similar movies by comparing their textual information.

The recommendation system uses **TF-IDF Vectorization** to convert movie text into numerical features and **Cosine Similarity** to identify movies with similar content.

## ✨ Features

- Recommend movies based on a selected movie title.
- Analyze movie genres and descriptions.
- Convert text into numerical vectors using TF-IDF.
- Calculate similarity scores using cosine similarity.
- Display the top 5 similar movie recommendations.
- Handle missing text values and invalid movie titles.

## 🛠️ Technologies Used

- **Python** — Core programming language
- **Pandas** — Dataset loading and manipulation
- **Scikit-learn** — Text vectorization and similarity calculations
- **Jupyter Notebook** — Development and experimentation

## 📂 Project Structure

```text
netflix-movie-recommender/
├── data/
│   └── movies.csv
| movie_recommender.ipynb
├── tf_env321/              # Local environment only; not committed
├── requirements.txt
├── README.md
└── .gitignore
```

*Note: The notebook and dataset filenames should match the actual files in your repository. The `tf_env321` virtual environment should remain local and should not be uploaded to GitHub.*

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/disham07/netflix-movie-recommender.git
cd netflix-movie-recommender
```

### 2. Create a virtual environment

```bash
python3 -m venv tf_env321
```

Activate it on macOS or Linux:

```bash
source tf_env321/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

The `requirements.txt` file should contain:

```text
pandas
scikit-learn
```

### 4. Prepare the dataset

Place your `movies.csv` file inside the `data/` directory.

The dataset should contain these columns:

- `title` — Movie title
- `genre` — Movie genre or genres
- `description` — Movie description

### 5. Run the project

Open Jupyter Notebook:

```bash
pip install notebook
jupyter notebook
```

Open your movie recommendation notebook and execute its cells in order.

## 🧠 How It Works

### Step 1: Data Preparation

The system loads the movie dataset and combines the genre and description into a single text field.

### Step 2: TF-IDF Vectorization

TF-IDF (Term Frequency–Inverse Document Frequency) converts textual information into numerical vectors. It gives greater importance to terms that help distinguish one movie from another.

### Step 3: Cosine Similarity

Cosine similarity compares the TF-IDF vectors to estimate how similar the movie content is.

### Step 4: Movie Recommendations

When a user enters a movie title, the system ranks the other movies by similarity and returns the top five results.

## 💻 Example Usage

```python
recommend_movies("The Hobbit", top_n=5)
```

Example output format:

```text
Movies similar to 'The Hobbit':
Movie A (similarity: 0.612)
Movie B (similarity: 0.487)
Movie C (similarity: 0.421)
```

*The titles and scores above are illustrative; actual recommendations depend on your dataset.*

## 📊 Recommendation Approach

**Type:** Content-based filtering

The system recommends movies based on similarities in their genres and descriptions rather than users' viewing histories or ratings.

## 🚀 Future Improvements

- Build an interactive web interface using Streamlit.
- Add movie posters and additional metadata.
- Improve text preprocessing and feature selection.
- Support partial title searches.
- Evaluate recommendation quality using suitable metrics.
- Expand the dataset with more movie information.

## ⚠️ Limitations

- Recommendations depend on the quality and completeness of the dataset.
- Movies with limited descriptions may receive less accurate recommendations.
- Similarity scores measure textual similarity, not necessarily audience preference.
- The system does not currently use collaborative filtering.

## 👩‍💻 Author

**Disha M.**

GitHub: [@disham07](https://github.com/disham07)

## 📄 License

This project is intended for educational and learning purposes. A license can be added to specify the terms under which others may use or distribute the code.
