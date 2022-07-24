# Analysis of Amazon Vine reviews for watches using Python (PySpark), AWS, Google Collab, and PostgreSQL to determine Bias

## Overview

The purpose of this project was to analyze Amazon reviews which were written by members of the paid Amazon Vine program. I chose a dataset of watch reviews located in an AWS S3 bucket, which can be accessed [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Watches_v1_00.tsv.gz). The goal is to determine if there is any bias when it comes to high ratings from users of the Vine program. This will be accomplished by using PySpark to perform the ETL process, connect to an AWS RDS instance, and load the data into pgAdmin. Then, PySpark will be used to perform the analysis and determine if there is any bias towards favorable reviews from the Vine members.

## Results

### Vine vs Non-Vine Reviews

#### Vine 

![Vine](./images/Vine%20Reviews.png)

- There are 47 total Vine reviews.

- Of the 47, 15 are 5 star reviews.

- 31.9% of the vine reviews are 5 stars.

#### Non-Vine

![Not Vine](./images/Not%20Vine%20Reviews.png)

- There are 8,362 total reviews which are not Vine members.

- Of the 8,362, there are 4,332 5 star reviews. 

- 51.8% of the non-vine reviews are 5 stars. 

## Summary

There is a major difference in the number of total paid (vine) and unpaid (not-vine) reviews, 47 and 8,362 respectively. This small number of vine reviews for this dataset may play a factor in the outcome. Moving on, 31.9% of the paid reviews and 51.8% of the unpaid reviews were 5 stars. This shows a possible negative bias towards the paid reviews. Additional analysis may be required to further support a conclusion that paid reviews produce a lower rating or fewer 5 star ratings. An analysis comparing the average rating of paid and unpaid reviews, regardless of the helpful/total votes, could prove beneficial. Doing this analysis without neglecting ratings which didnt receive a certain # of total or helpful votes would provide a larger dataset to work with and may produce a different outcome. 
