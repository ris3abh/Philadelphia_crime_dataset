# Philadelphia crime dataset

This is the final project for DSCI-511 Class, where we need to create a dataset using data extraction, data cleaning and various pre-processing tasks. 

We first extracted raw data from OpenDataPhilly to get the Crime Database for the year 2022 in the form of a CSV file. We then extract the timestamps and date, use those as endpoint parameters for the "Weather Api" to get the weather data and form a big dataset. By extracting the timestamps and date, we can communicate with the Holiday API to get the list of special events or holidays happening at that time. We then use those same timestamps to retrieve 
information from a Stock market API to get the daily/historical stock market data and add those information to create an even larger dataset. Using various libraries like twython, tweepy and others, we will extract data from several accounts which are active in displaying the crime data. 

Using BeautifulSoap we performed webscrapping on the True Crime daily dataset for philadelphia and extracted all the data availbale till November 26th 2022. 

API's used-
1. Stock Data:  Using the alpha vantage API we collected the opening closing volume and other data for each date, The data was easily accessible using the API, we chose to go with the API form of collection. for each day the dataset shows us the value of stocks after each hour.(https://www.alphavantage.co/)

2. holiday API: Using the holiday API we were able to pin point if a given day would be a holiday or not. This can be used later to notice if crime rates are high or low during the holiday seasons.(https://holidayapi.com/v1/holidays?pretty&key=e1df5793-02a5-4982-bf6d-df30497e8305&country=US&year=2021)

3. weather API: Using the weather API we were able to pin point the weather on the given day. This can be used later to notice if crime rates are high or low during certain seasons seasons and other climate attributes.(http://api.weatherapi.com/v1/history.json?key=2eec0b76d1b24fe28c5164334222511&q=Philadelphia&dt='+date)


4. Twitter API: using the twitter API elevated access, we generated tokens and used them to extract data from the twitter handle of Philadelphia Police, Which gives live reporting of criminal activities in the philadelphia region. The dataset has 5 attributes namely - tweets, created_at, the user who posted it, likes, retweets and the link to the tweet. This can be used in various ways by the philadelphia police, philadelphia public safety, drexel and Upenn Police departments and others as well. The twitter text data can be used to understand the nature of crimes in the philadelphia region.(https://developer.twitter.com/en/docs/twitter-api)

5. True Crime daily scraping: Using beautifulSoup and requests we web scrapped the data from the true crime daily website, this is essentialy a news blog for the USA, On the website we scarpped data for the crimes which have happened in the philadelphia region. From the initial page, we were able to extract all the links to the blog post about individual crimes and their detailed text. This dataset has 5 columns - links, titles, text, date and time. This can be used in a similar way as the twitter API.( https://truecrimedaily.com/search/?q=philadelphia&page=2)

These datasets can not be merged with the crime and weather dataset as the crimes reported in the crime and weather dataset can vary from the twitter and true crime daily dataset.
