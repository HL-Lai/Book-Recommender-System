# Book Recommender System

This repository contains the code for a book recommendation system. The system uses collaborative filtering techniques to recommend books to users based on their past ratings.

## Overview

The recommendation system is built using the Surprise library, which is a Python scikit for building and analyzing recommender systems. The system uses three algorithms for making predictions: Singular Value Decomposition (SVD), Non-negative Matrix Factorization (NMF), and NormalPredictor.

The system also uses GridSearchCV to find the best hyperparameters for the SVD algorithm, which is then used to train the model on the entire dataset.

## Data Source
The data used in this project is sourced from [Kaggle](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset?select=Books.csv). The dataset contains detailed information about various books, including their titles, authors, publication year, and user ratings.

## Usage

The system takes as input a user ID and outputs a list of recommended books for that user. If no user ID is provided, the system will randomly select a user and provide recommendations for them.

## Code Structure

The code is structured as follows:

1. Preprocess the data.
2. Define the algorithms to be used.
3. Cross-validate each algorithm on the data.
4. Set up the Surprise Dataset and Reader objects.
5. Define the parameter grid to search over.
6. Set up and run the GridSearchCV object.
7. Print the best RMSE score and the combination of parameters that gave the best RMSE score.
8. Set up the Surprise Dataset and Reader objects again, this time with a different rating scale.
9. Split the data into training and test sets.
10. Set the best hyperparameters found during grid search.
11. Train the SVD model on the entire dataset using the best hyperparameters.
12. Define a function to make recommendations.
13. Call the recommendation function, passing in a user ID or leaving it blank for a random user.

## Future Work

Future improvements to this system could include implementing more sophisticated recommendation algorithms, incorporating additional user and item features into the model, and building a user interface for interacting with the system.

## Reference
Mobius. (2021). Book Recommendation Dataset, Version 1. Retrieved March 19, 2023 from https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset?select=Books.csv