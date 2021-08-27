# Movies-ETL
M8 ETL - Extract, Transform, Load
## Project Overview
To prepare the clean dataset for the hackathon, this project will create an automated pipeline that takes in new data from Wikipedia data, Kaggle metadata, and the MovieLens rating data. And then, it will perform the ETL process by adding the data to a PostgreSQL database.

## Process & Results
-	Write an ETL Function to Read Three Data Files

  [ETL_function_test.ipynb](https://github.com/BessHung/Movies-ETL/blob/007aea6fa9786bfa907aa4c8e586671a2d3f70bb/ETL_function_test.ipynb)

1. Read in the Wikipedia data JSON file, kaggle metadata and MovieLens ratings CSV files as Pandas DataFrames.

-	Extract and Transform the Wikipedia Data

[ETL_clean_wiki_movies.ipynb](https://github.com/BessHung/Movies-ETL/blob/007aea6fa9786bfa907aa4c8e586671a2d3f70bb/ETL_clean_wiki_movies.ipynb)
1.	Create function to clean and merge columns
2.	Extract “imdb_id” from 'imdb_link' by using regex statement
3.	Write regular expressions and create the function to parse the data in columns of “Box office” and “Budget, “Release date” and “Running time”

-	Extract and Transform the Kaggle data

[ETL_clean_kaggle_data.ipynb](https://github.com/BessHung/Movies-ETL/blob/007aea6fa9786bfa907aa4c8e586671a2d3f70bb/ETL_clean_kaggle_data.ipynb)
1.	Check and convert the columns into correct data types.
2.	Remove Bad Data
3.	Merged the two Wiki movies dataset and Kaggle dataset into the movies DataFrame.
4.	Drop unnecessary columns from the merged DataFrame.
5.	Transform and merge the ratings data into movies_with_ratings_df DataFrame 
-	Create the Movie Database

[ETL_create_database.ipynb](https://github.com/BessHung/Movies-ETL/blob/007aea6fa9786bfa907aa4c8e586671a2d3f70bb/ETL_create_database.ipynb)
1.	Create the Database Engine
2.	Import the Movie and Data to PostgreSQL


###### The rows of movies data
![](https://github.com/BessHung/Movies-ETL/blob/007aea6fa9786bfa907aa4c8e586671a2d3f70bb/Resources/movies_query.png)

###### The rows of rating data
![](https://github.com/BessHung/Movies-ETL/blob/007aea6fa9786bfa907aa4c8e586671a2d3f70bb/Resources/ratings_query.png)
