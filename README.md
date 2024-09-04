# Movie Recommendation System
This project is a Movie Recommendation System built using the TMDb 5000 Movies and Credits Dataset. The system allows users to explore movies, view detailed information, and receive recommendations based on different movie features like genres, keywords, cast, and crew.

- Table of Contents
- Introduction
- Dataset
- Installation
- Usage
- Features
- Data Preprocessing
- Recommendation Algorithm
- Results
- Contributing
- License
- Acknowledgements

## Introduction
This project demonstrates how to build a Movie Recommendation System using data from TMDb. The project involves data preprocessing, feature extraction, and the - - application of recommendation algorithms to suggest movies based on user preferences.

## Dataset
The dataset used in this project is the TMDb 5000 Movies and Credits dataset, available on Kaggle. It consists of two main CSV files:

- `tmdb_5000_movies.csv`: Contains information about movies, including budget, genres, popularity, revenue, runtime, and more.
- `tmdb_5000_credits.csv`: Contains information about the cast and crew of each movie.

## Installation
To get started with the project, clone the repository and install the required dependencies:

Copy code
```
git clone https://github.com/yourusername/movierecommendation.git
cd movierecommendation
pip install -r requirements.txt
```
## Usage
To run the project, follow these steps:

Ensure that you have the dataset files in the appropriate directory.
Load the dataset and run the Jupyter notebook or Python script provided to preprocess the data and generate recommendations.

## Example usage in a Jupyter notebook:
```
python
Copy code
import pandas as pd

# Load the data
movies = pd.read_csv('tmdb_5000_movies.csv')
credits = pd.read_csv('tmdb_5000_credits.csv')

# Data preprocessing and model training
# ...

# Get recommendations
recommendations = get_recommendations('Avatar')
print(recommendations)
```

## Features
- Data Merging: The movies and credits datasets are merged on the title column to combine relevant information.
- Data Preprocessing: The dataset is cleaned by removing missing values and converting JSON-like fields into usable lists.
- Feature Extraction: Extracts key features like genres, keywords, cast, and crew to be used in the recommendation algorithm.
- Recommendation Engine: The system recommends movies based on similarity measures computed using the extracted features.

## Data Preprocessing
The preprocessing steps include:

- Merging the `movies` and `credits` datasets.
- Parsing JSON-like strings in columns such as `genres`, `keywords`, `cast`, and `crew` to extract meaningful information.
- Limiting the number of features in the `cast` column to focus on the top 3 actors.
- Handling missing values by dropping rows with null values.

## Recommendation Algorithm
The recommendation engine uses cosine similarity to measure the similarity between movies based on selected features. The algorithm suggests movies that are similar to a given movie based on the features such as genres, keywords, and cast.

## Results
The recommendation system can provide suggestions for similar movies when a movie title is provided. These recommendations are based on the extracted features and the similarity calculations performed by the algorithm.

## Acknowledgements
- The TMDb 5000 Movies Dataset was sourced from Kaggle.
- Inspiration and guidance were drawn from various online resources and tutorials.
