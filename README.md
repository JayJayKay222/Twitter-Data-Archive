It contains data from a Twitter Account @dog_rates who rates people's dogs with a humorous comment about the dog.

• Gathering Data -
The data used for thus project was gathered from 3 sources

(i) Twitter-Archive-Enhanced -
This data was downloaded manually from the provided link on the Udacity workspace and then uploaded on the machine and eventually read as a csv file into Pandas dataframe programmatically.

(ii) Image Predictions
This was extracted by downloading the file programmatically using Requests library from the provided link. This data is. every image in the WeRateFogs Twitter archive through a neural network thaat classifies dogs into breeds.

(iii) tweet.json.tst
This is an additional Twitter API data. It was obtained from querying the Twitter's API and then stored as txt file which was read line by line into pandas Dataframe.

NOTE: Gathering this data requires a Twitter developer account but thee data used in this project were the provided data by Udacity.   I couldn't get access to the developer account.


• Assessing Data -
After the gathering process the dataa extracted were assessed visually and programmatically to find Quality(content) issues and Tidiness(structural) issues before cleaning.

A. Twitter-Enhanced-Archive
• Some rows are actually Retweets and not original tweets(which is needed for the analysis) • This confirms that the rating_denominator and rating_numerator have inconsistent data maybe due to recording data not related, not properly recording the values • The Timestamp column is a object data type instead of datetime • Timestamp column has extra characters +0000 • Text column has links attached to it(This was not attended to in the cleaning process) • Dog stages are not in the same column

B. Image-Predictions Data
• The p1_dog column has false values that indicate that some rows are not a breed of dog • We only need these columns for the analysis = tweet_id, img_num, breed, confidence_level, p1_dog

C. Tweets Data -
• The tweet_id column name appears to be id in this table • We only need the tweet_id, retweet_count and favourite_count columns



• STORING DATA
The 3 data (twitter-enhanced-archive, tweets.json.txt, image-predictions.tsv) assessed and cleaned in the wrangle process were merged into one data which was stored in csv format. This stage was performed using pandas to save the data as 'twitter-archive-master.csv' which wwas then used for the analyzing and visualizing stage.

• DATA VISUALIZATION
Three questions were answered here which includes one visualization

1. What are the most common dog stages?
In the visualization theis question was answered thata PUPPER is the most common dog stage

2. Which is the most common breed?
golden_retriever appears to be the most common breed of dog with 138 count

3. Which dog stage has the highest rating?
DOGGO, PUPPO has the highest average rating
