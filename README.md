# A simple-Spotify-ETL

Task 1: Lets call it exchange_Token,
In this Task we will be the function exchanges an authorization code for Spotify access and refresh tokens by sending a POST request to Spotify’s token endpoint.
It constructs the payload with credentials and prints the authorization code. If the request is successful, it retrieves and stores the access and refresh tokens in Airflow variables. If the request fails, it prints the error response.
In this code we are exchanging tokens with API and setting up the variables in the Airflow which we will be using it later on.

Task 2: Will call this refresh_token,
In this task our function refreshes the Spotify access token using the stored refresh token. It retrieves the refresh token from Airflow variables and sends a POST request to Spotify’s token endpoint with the appropriate payload. It prints the refresh token and, if the request is successful, updates the access token in Airflow variables and prints the new access token. If the request fails, it prints the error response.

**Task 3: Lets call it get_songs, here we will be pulling “song_name”, “artist_name”, “played_at”, “timestamp” from the json and then using Connection String will be creating sql engine for our MySQL db and then pushing all the data into the DB.
This task will basically calls the API GET request with the UnixTimestamp and will receive a JSON request from the server which later will be converting into a dataframe. This dataframe will be sending to our desired database (in this case mysql).**

