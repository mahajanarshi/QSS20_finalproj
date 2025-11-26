# QSS20_finalproj

Our main datasets are as follows:
1) The Climate Change Twitter Dataset - https://www.kaggle.com/datasets/deffro/the-climate-change-twitter-dataset
2) Twitter datasets:
    - 2018 twitter df - https://www.kaggle.com/datasets/edqian/twitter-climate-change-sentiment-dataset
    - 2020 twitter df - https://www.kaggle.com/datasets/joseguzman/climate-sentiment-in-twitter
    - 2022 twitter df - https://www.kaggle.com/datasets/die9origephit/climate-change-tweets
3) Natural Disasters Information from EMDAT - https://www.emdat.be/
4) World Bank Dataset, GDP per Capita - https://data.worldbank.org/indicator/NY.GDP.PCAP.CD

All scripts are in the "scripts" folder and all cleaned datafiles and figures are in the "outputs" folder.

Our analysis proceeded in two parts, focusing on analyzing the contents of the tweets (with the datasets under the "Twitter datasets" links above) and the already created sentiment scores by natural disasters (using datasets 1, 3, and 4 above). 

Cleaning and preprocessing for the first part of the analysis involved converting to lowercase, tokenizing, removing numbers and links, converting to stems, using custom stopwords, and removing all words that are less than 4 characters long. Then, a sentiment analysis was conducted on tweets, along with wordcloud creation and topic identification. This allowed us to analyze how overall sentiment and content of tweets shifted in Twitter discourse over time. Packages VADER and Wordclouds was used for processing and visualization, and an LDA model was used for topic identification. 

Cleaning and preprocessing for the second part of analysis involved using packages reverse_geocoder and pycountry to convert latitude and longitude values to full country names. Percent change in GDP per capita was also added using the World Bank dataset (using the year before the disaster as a baseline, and the year after as the "post"). Merging this with the Climate Change Tweet Database allowed for our tweet-level dataset to be formed. Additionally, we created a database that was country-level, with the average sentiment score for each year.
