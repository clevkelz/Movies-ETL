# Movies-ETL

This analysis builds on the work previously done to 
- Extract movie data from Wikipedia and Kaggle.  The Kaggle data had two sets of files:  the movie metadata and then the MovieLens rating file.
- Transform, clean, and then combine the data.
- Load the cleaned data into a SQL database.

Originally the transformation and loading steps were done through multiple lines of code to individually identify the incomplete, inconsistent, and duplicate data.  These steps are included in this GitHub repository under the MergedMovies Jupyter Notebook file.  The challenge assignment refactors this code to create one function that takes in the three files (Wikipedia data, Kaggle metadata, and MovieLens rating data), transforms the data, and then adds the data to the PostgresSQL database.  The refactored code is housed in this GitHub repository.  There are four files as noted below but they all build on each other and use the same function (which is modified and added to for each step).  These files are:
1. ETL_function_test.ipynb:  Establishes the function to take in the three files.
2.	ETL_clean_wiki_movies.ipynb: Creates the code to clean up the Wikipedia data
3.	ETL_clean_kaggle_data.ipynb – Creates the code to clean up the Kaggle metadata and MovieLens rating data
4.	ETL_create_database.ipynb – Creates the code to take the merged Wikipedia and Kaggle movie data and send that to PostgresSQL as a database.  This code also takes the ratings data and creates a database for that dataset.

There are also two screenprints to show that the merged movies and ratings database were successfully loaded into PostgresSQL.

The original Wikipedia and Kaggle metadata have also been loaded to this repository.  The Kaggle metadata had to be zipped because it was too large to store in the original format.  The ratings data is over 700 MB and cannot be stored on GitHub.



