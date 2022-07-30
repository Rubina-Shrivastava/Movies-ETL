# Movies-ETL
## Purpose:
### Amazing Prime loves the dataset and wants to keep it updated on a daily basis for that we have to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables.
## Challenge:
### WE need to refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.
## Recourses :
### Software: pgAdmin, Python, Visual Studio Code 
### Data Tools: PostgreSQL, pgAdmin, Anaconda prompt, Jupyter Notebook
## Result :
### 1: ETL Function to Read Three Data Files
 #### Read in the Kaggle metadata and MovieLens ratings CSV files as Pandas DataFrames, opened the Wikipedia JSON file, and use the JSON. load() function to convert the JSON data to raw data and creating the Wikipedia data, the Kaggle metadata, and the MovieLens rating data files.
 ### Wikipedia data Image
 ### Kaggle metadata Image
 ### rating data Image
### 2: Extract and Transform the Wikipedia Data
####  With the help of regular expression  and list comprehension, the following columns are cleaned in the Wikipedia DataFrame:
#### The box office column
#### The budget column
#### The release date column
#### The running time column
### wiki_movies_df DataFrame Image 
### wiki_movies_df DataFrame columns Image
### 3: Extract and Transform the Kaggle data
#### Merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame then merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df so The Kaggle metadata is cleaned and The Wikipedia and Kaggle DataFrames are merged.
### Movies_df Image
### Movies_with_rating_df Image
### 4: Create the Movie Database
#### The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database and the data from the MovieLens rating CSV file is added to the ratings table in the SQL database.
### Ratings_query Image
### movie_query Image
#### The data from the rating CSV file is added to the ratings table in the SQL database 
#### The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file