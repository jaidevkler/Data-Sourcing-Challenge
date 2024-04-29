# Data Sourcing Challenge
Module 6 Challenge prepares some data for a recommendation system to help people find movie reviews and related movies. The program extracts data from two different sources: The New York Times API and The Movie Database, then merges the data together. The extracted data can be later used for NLP methods. 

## Code Source
The code location is: [Click Here to view](https://github.com/jaidevkler/data-sourcing-challenge)

## Files
* retrieve_movie_data.ipynb [Click here to view](https://github.com/jaidevkler/data-sourcing-challenge/blob/main/retrieve_movie_data.ipynb)<br />
* README.md [Click here to view](https://github.com/jaidevkler/data-sourcing-challenge/blob/main/README.md)<br />
* nyt_tmdb_df.csv [Click here to view](https://github.com/jaidevkler/data-sourcing-challenge/blob/main/nyt_tmdb_df.csv)<br />

## How to run the program
Download the files and then use jupyter notebook or jupyter lab to open the retrieve_movie_data.ipynb file.

## Program
### 1. Access the New York Times API
* The program first prepares a query url with the base url, API key, query, sort filter, field list and data range.
* Since the NYT API limits results to 10 per page a for loop is used to retrive 200 results over 20 pages.
* The url is then further modified to include the page number. This url is used to get review data from the NYT server.
* Another loop is used to loop through the obtained data to append each review to the review list.
* The reviews list is then convered into a datafram using json_normalized() function
* The title is extracted from 'headline.main' column using the lambda function provided.
* The keywords column is convered to strings using the extract_keywords function() provided.
* A list of titles is created by using the to_list() function on the 'title' column

### 2. Access the Movie Database API
* A for loop is used to loop through the list of titles.
* A counter is used in order to make the program sleep for a second after every 50 requests. A message is also printed to let the user know that the program is sleeping.
* The movie database url is then used to get movies data from the server.
* Genres, spoken languages and production countries are extracted from the data obtained using list comprehensions. This data is then added to the tmdb_movies_list in a dictionary form along with the other chosen fields.
* The program prints an error message in case if the data title was not found else prints that it was found.
* The dictoionary is then converted into a dataframe called tmdb_df

### 3. Merge and Clean the Data the Export
* The NYT and Movies Dataframes are merged on title using the merge() function.
* The genres, spoken languages and production countries columns are converted to strings. Box brackets and quotes are removed from the strings.
* The 'byline.person' column is dropped from the merged dataframe.
* Any duplicaate rows are dropped from the dataframe
* The index of the dataframe is then dropped to give us our final dataframe.
* The dataframe is saved to file called 'nyt_tmdb_df.csv' using the to_csv() function

## Conclusion
The assignment shows how to source data from different websites using their API.

