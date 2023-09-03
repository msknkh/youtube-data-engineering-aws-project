# Complete Data ETL on AWS using Glue, Lambda, Athena and S3

We used Trending Youtube Video Statistics data (https://www.kaggle.com/datasets/datasnaek/youtube-new)

## Steps we took to approach the problem 

1. This was a complex data that we loaded onto the raw S3 bucket on Amazon to begin our process of cleaning and transforming the data.

2. This data had both csv and json files relevant to youtube video statistics in different regions

3. Due to json data, we had to write Lambda function to convert the json data to parquet file to further process the data

4. After successfully crawling the json data, we crawl the csv data, where we use the pyspark code in glue editor to specify how we want the cleaned data to look.

5. Then we join both the statistics and category data tables using Glue Pyspark script (or GUI) and store it to the S3 bucket.

6. The data is ready for analytics finally :)

