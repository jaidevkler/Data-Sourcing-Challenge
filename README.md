# Data Sourcing Challenge
Module 6 Challenge prepares some data for a recommendation system to help people find movie reviews and related movies. The program extracts data from two different sources: The New York Times API and The Movie Database, then merges the data together. The extracted data can be later used for NLP methods. 

## Code Source
The code location is: [Click Here to view](https://github.com/jaidevkler/data-sourcing-challenge)

## Files
* retrieve_movie_data.ipynb [Click here to view](https://github.com/jaidevkler/data-sourcing-challenge/blob/main/retrieve_movie_data.ipynb)<br />
* README.md [Click here to view](https://github.com/jaidevkler/data-sourcing-challenge/blob/main/README.md)<br />
* merged_index.csv [Click here to view](https://github.com/jaidevkler/data-sourcing-challenge/blob/main/merged_index.csv)<br />

## How to run the program
Download the files and then use jupyter notebook or jupyter lab to open the retrieve_movie_data.ipynb file.

## Program
### 1. Access the New York Times API
* The program first prepares a url with the API key, query, sort filter, field list and data range.
* This url is used to get data from the NYT server. The data is then converted into a data frame using the json_normailize() function.
* A list of unique writers is extracted and saved from the 'byline.orginal' column of the data frame.

### 2. Access the Movie Database API
* A for loop is used to loop through the list of unique writers.
* Within the loop a url is created and used to get 


### 3. Merge and Clean the Data the Export


## Conclusion
The assignment shows how different function (concat, groupby, pivot, resample) can be used to combine and sort data to analysis the data for better decision making.

