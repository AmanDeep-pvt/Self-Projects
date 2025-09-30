Movie Recommendation System
This project implements a movie recommendation system using the MovieLens dataset. It provides movie suggestions based on two different filtering techniques: Content-Based Filtering and Collaborative Filtering.

Features
Content-Based Filtering: Recommends movies based on their genre similarity. It uses TF-IDF vectorization to process movie genres and calculates cosine similarity to find similar movies.

Collaborative Filtering: Recommends movies by analyzing the behavior of users. This implementation uses the Singular Value Decomposition (SVD) algorithm from the surprise library to predict movie ratings a user might give.

Data Visualization: Includes functions to visualize the distribution of user ratings and to display the top 5 recommendations for a given movie using matplotlib and seaborn.

Dataset
This project uses the "small" MovieLens dataset, which is suitable for experimentation on personal computers. It consists of:

ratings.csv: Contains userId, movieId, rating, and timestamp.

movies.csv: Contains movieId, title, and genres.

You can download the dataset from the GroupLens website: MovieLens Latest Datasets. Please download the ml-latest-small.zip file and extract ratings.csv and movies.csv into the same directory as the project script.

Setup and Installation
Clone the repository (or download the files):

git clone [https://github.com/your-username/movie-recommendation-system.git](https://github.com/your-username/movie-recommendation-system.git)
cd movie-recommendation-system

Create a virtual environment (recommended):

python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

Install the required dependencies:
Make sure you have the requirements.txt file in your project directory.

pip install -r requirements.txt

Usage
To run the recommendation system, execute the main script from your terminal:

python movie_recommender.py

The script will:

Load and preprocess the MovieLens data.

Train the collaborative filtering model (SVD).

Generate and print the top 5 movie recommendations for a predefined target movie (e.g., 'Forrest Gump (1994)') using both methods.

Display two plots:

A bar chart showing the distribution of all movie ratings in the dataset.

Bar charts illustrating the top 5 recommendations from each filtering method for the target movie.

Example Output
Movie Recommendation System

Target Movie: Forrest Gump (1994)

Content-Based Recommendations
      1. Apollo 13 (1995)
      2. Wag the Dog (1997)
      3. Saving Private Ryan (1998)
      4. Good Will Hunting (1997)
      5. Erin Brockovich (2000)

========================================

Collaborative Filtering Recommendations
      1. Shawshank Redemption, The (1994)
      2. Pulp Fiction (1994)
      3. Silence of the Lambs, The (1991)
      4. Matrix, The (1999)
      5. Star Wars: Episode IV - A New Hope (1977)

========================================

Displaying visualization for overall movie ratings distribution...
(A plot window will open)

Displaying visualization for Content-Based recommendations for 'Forrest Gump (1994)'...
(A plot window will open)

Displaying visualization for Collaborative Filtering recommendations for 'Forrest Gump (1994)'...
(A plot window will open)


You can easily change the target_movie variable in the if __name__ == '__main__': block of movie_recommender.py to get recommendations for a different film.****
