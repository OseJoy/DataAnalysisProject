# DataAnalysisProject - WeRateDogs Twitter Archive
## Introduction
In this project, the dataset I will be wrangling, analyzing and visualizing is the tweet archive of Twitter user **@dog_rates**, also known as **WeRateDogs**. **WeRateDogs** is a 
Twitter account that rates people's dogs with a humorous comment about the dog. 
The tasks for this project were:
- Data wrangling, which consisted of:
  - Gathering data
  - Assessing data
  - Cleaning data
- Storing, analyzing, and visualizing the wrangled data
- Reporting on 
  - my data wrangling efforts
  - my data analyses and visualizations (act_report.pdf)

## Data
**WeRateDogs** provided their Twitter archive (which included tweets through August 1, 2017) of basic tweet data (tweet ID, timestamp, text, etc.) for use with this project.
The "enhanced" csv file provided by Udacity (twitter_archive_enhanced.csv) also contains columns which were extracted programatically: the rating numerator, rating 
denominator, dog's name, and dog stages (doggo, floofer, pupper, and puppo). These columns needed to be assessed and cleaned as the extraction process wasn't perfect.

The provided Twitter archive lacked some useful information: retweet count and favorite count. I used the tweet IDs to query the Twitter API for each tweet's JSON data 
using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt. I then read the txt file line by line into a pandas 
DataFrame only including the desired variables; retweet count and favorite count.

Udacity also provided a link to image_predictions.tsv which I downloaded programatically using the Requests library.
