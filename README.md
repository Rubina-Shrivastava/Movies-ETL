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
![Wikipedia Data Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/wiki_movies_df.png)
 ### Kaggle metadata Image
![Kaggle Metadata Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/kaggle_metadata.png)
 ### rating data Image
![Rating Data Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/ratings%20.png)
### 2: Extract and Transform the Wikipedia Data
####  With the help of regular expression  and list comprehension, the following columns are cleaned in the Wikipedia DataFrame:
#### The box office column
#### The budget column
#### The release date column
#### The running time column
### wiki_movies_df DataFrame Image 
![Wiki Movies DF Data Frame](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/wiki_movies_df2.png)
### wiki_movies_df DataFrame columns Image
![Wiki Movies Data Frame Column Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/columns%20from%20wiki_movies_df.png)
### 3: Extract and Transform the Kaggle data
#### Merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame then merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df so The Kaggle metadata is cleaned and The Wikipedia and Kaggle DataFrames are merged.
### Movies_df Image
![Movie DF Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/movies_df.png)
### Movies_with_rating_df Image
![Movies with Rating DF](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/movies_with_ratings_df.png)
### 4: Create the Movie Database
#### The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database and the data from the MovieLens rating CSV file is added to the ratings table in the SQL database.
### Ratings_query Image
![Ratings Query Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/ratings_query.png)
### movie_query Image
![Movie Query Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/movies_query.png)
#### The data from the rating CSV file is added to the ratings table in the SQL database 
![Coding Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/Importing%20data%20.png)
#### The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file
![Coding Image](https://github.com/Rubina-Shrivastava/Movies-ETL/blob/main/elapsed%20time%20to%20add%20the%20data.png)
