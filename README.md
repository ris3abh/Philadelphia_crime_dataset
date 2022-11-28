# Philadelphia crime dataset

This is the final project for DSCI-511 Class, where we need to create a dataset using data extraction, data cleaning and various pre-processing tasks. 

We first extracted raw data from OpenDataPhilly to get the Crime Database for the year 2022 in the form of a CSV file. We then extract the timestamps and date, use those as endpoint parameters for the "Weather Api" to get the weather data and form a big dataset. By extracting the timestamps and date, we can communicate with the Holiday API to get the list of special events or holidays happening at that time. We then use those same timestamps to retrieve 
information from a Stock market API to get the daily/historical stock market data and add those information to create an even larger dataset. Using various libraries like twython, tweepy and others, we will extract data from several accounts which are active in displaying the crime data. 

Using BeautifulSoap we performed webscrapping on the True Crime daily dataset for philadelphia and extracted all the data availbale till November 26th 2022. 

API's used-
1. Twitter API: https://developer.twitter.com/en/docs/twitter-api
2. Stock Data:  https://www.alphavantage.co/
3. True Crime daily data:  https://truecrimedaily.com/search/?q=philadelphia&page=2
4. holiday API: https://holidayapi.com/v1/holidays?pretty&key=e1df5793-02a5-4982-bf6d-df30497e8305&country=US&year=2021
5. weather API: http://api.weatherapi.com/v1/history.json?key=2eec0b76d1b24fe28c5164334222511&q=Philadelphia&dt='+date

