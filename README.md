Movie Recommender System

This project is a **Movie Recommender System** built using **Streamlit**. The app suggests movies based on the similarity between them using a pre-trained model. The movie data is fetched from **The Movie Database (TMDb)** API, and movie posters are displayed along with recommendations.

Installation

To run the code, you need to install the following libraries:

pip install streamlit pandas requests

If you're using a virtual environment, make sure to activate it before running the above commands.

How the Code Works

Streamlit and Pickle are used to create the user interface and load pre-trained models (movie data and similarity scores). Pandas manages the movie dataset, and Requests fetches data from the TMDb API, including movie posters.

Code Explanation

The app title is set using st.title('Movie Recommender System').

Function: fetch_poster(movie_id)

This function retrieves the movie poster from the TMDb API using the movie ID. It formats the API response into a complete URL for the poster image.

Function: recommend(movie)

Finds the selected movie's index and retrieves a list of similar movies using the similarity scores. It fetches the top 5 most similar movies and their posters by calling fetch_poster(). Returns the list of recommended movie names and poster URLs.

Main App Flow

A selectbox allows the user to choose a movie. When the user clicks the "Show Recommendation" button, the app calls the recommend() function, displaying the top 5 recommended movies with their posters in a grid.

Dataset

The dataset used in this project can be downloaded from the Kaggle TMDb Movie Metadata page: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?resource=download
Download the dataset or extract the required data from the .rar file. Place it in the project repository and use it as per the instructions in the code.

TMDb API

This project uses the TMDb API to fetch additional data such as movie posters. You will need to create an API key from TMDb to use this functionality. Visit the TMDb API for more information: https://developer.themoviedb.org/v4/reference/intro/getting-started

File Requirements

Ensure that the following files are present in the repository for the code to run properly:

movies.pkl: Pickle file containing movie data.
similarity.pkl: Pickle file containing similarity scores between movies.
How to Run the App

Download or clone the repository.
Ensure you have installed the required libraries.
Run the following command to start the Streamlit app:

streamlit run app.py

The app will open in your browser, and you can start using the movie recommendation system.

Modules Used

Streamlit: Interactive web interface
Pandas: Handling the movie dataset
Requests: Fetching movie posters from TMDb
Pickle: Loading pre-trained models
License

This project is licensed under the MIT License. You are free to use, modify, and distribute the code under the terms of the license.

Copyright

The movie data is provided by The Movie Database (TMDb). This product uses the TMDb API but is not endorsed or certified by TMDb.

Note: Ensure that you adhere to TMDb's terms of service when using the API in your project.

© 2024 Prem Kumar. All rights reserved.
