# Movie Recommendation System

## Overview

This project aims to create a movie recommendation system using collaborative filtering techniques. The system recommends movies based on user ratings, leveraging the power of machine learning algorithms to provide personalized recommendations.

## Dataset

The project uses a dataset consisting of two main files:
- `movies.csv`: Contains movie information such as `movieId` and `title`.
- `ratings.csv`: Contains user ratings for different movies, including `userId`, `movieId`, and the `rating` given.

## Key Steps

### Data Loading and Exploration

1. **Load Datasets**: Load the movies and ratings datasets using pandas.
2. **Inspect Datasets**: Inspect the first few rows of each dataset to understand their structure.

### Data Preparation

1. **Unique Users and Movies**: Calculate the number of unique users and movies.
2. **Sparsity Calculation**: Compute the sparsity of the user-item matrix to understand how sparse the data is.
3. **Ratings Distribution**: Plot the distribution of ratings to see which ratings are more frequent.
4. **Movie and User Frequency**: Plot the frequency of ratings per movie and per user to identify popular movies and active users.

### Filtering

1. **Popular Movies**: Filter out movies that have been rated less than a specified threshold.
2. **Active Users**: Filter out users who have rated less than a specified threshold.
3. **Final Ratings DataFrame**: Create a final filtered ratings DataFrame containing only popular movies and active users.

### Matrix Creation

1. **Item-User Matrix**: Create an item-user matrix with movies as rows and users as columns, filling missing values with zeros.
2. **Sparse Matrix**: Convert the item-user matrix to a sparse matrix format for efficient computation.

### Recommendation Model

1. **Movie Index Mapper**: Create a mapper to map movie titles to their corresponding indices in the item-user matrix.
2. **Nearest Neighbors Model**: Define and train a Nearest Neighbors model using cosine similarity.

### Fuzzy Matching

1. **Fuzzy Matching Function**: Implement a function to perform fuzzy matching of movie titles to handle typos and variations in input.

### Recommendations

1. **Generate Recommendations**: Use the trained model to generate and print movie recommendations based on a provided movie title.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ii_ruks/Movie-Recommendation-System.git
   cd MovieRecommendation
