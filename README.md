# Movies-ETL
#
## Aggregation and Organization of movie data
#
### Deliverable 1 - An ETL Function to Read Three Data Files
#
* An ETL function is written to read in the three data files.  
* The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.  
* ​The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.  
* ​The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.  
#
### Deliverable 2 - Extract and Transform the Wikipedia Data
#
* The TV shows are filtered out, and the wiki_movies_df DataFrame is created. 
* A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs. 
* The extraction and transformation of the Wikipedia data in the ETL function does the following:
* A list comprehension is used to keep columns with non-null values. 
* The non-null box office data is converted to string values using the lambda and join functions. 
* A regular expression is used to match the six elements of "form_one" of the box office data. 
* A regular expression is used to match the three elements of "form_two" of the box office data. 
* The following columns are cleaned in the Wikipedia DataFrame: 
* The box office column
* The budget column
* The release date column
* The running time column
* ​The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file. 
#
### Deliverable 3 - Extract and Transform the Kaggle Data 
#
* The extraction and transformation of the Kaggle metadata using the ETL function does the following:
    * The Kaggle metadata is cleaned. 
    * The Wikipedia and Kaggle DataFrames are merged. 
* The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df: 
    * Unnecessary columns are dropped.
    * A function is used to fill in the missing Kaggle data.
    * The movies_df DataFrame is filtered to keep specific columns.
    * The movies_df DataFrame columns are renamed.
    * The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
    * The ratings counts are cleaned. 
* The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame. 
* The empty values in the movies_with_ratings_df DataFrame are filled with “0”. 
* The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file. 
#### Deliverable 4 - Create the Movie Database
#
* Upload the following to your Movies-ETL GitHub repository:
    * The ETL_function_test.ipynb file
    * The ETL_clean_wiki_movies.ipynb file
    * The ETL_clean_kaggle_data.ipynb file
    * The ETL_create_database.ipynb file
* The Resources folder with the wikipedia_movies.json, movies_metadata.csv, movies_query.png, and ratings_query.png files.
* A README.md that describes the purpose of the repository. 