# QTM350 Final Project
This is our team's work for the final project for QTM 350 (Spring '21)

By: Laura Neff, Jason Hamilton, Jason Perelman, and Chris Nicholson

In this project, we will collect written movie reviews, perform sentiment analysis using [AWS Comprehend](https://aws.amazon.com/comprehend/), and then analyze Comprehend's accuracy using a variety of statistical techniques. We will be using two different corpora of movie reviews specifically designed for sentiment analysis projects: 1) the Cornell Movie Reviews Database, which includes 5,006 movie reviews and ratings (0-1) by four different authors, and 2) the Rotten Tomatoes Movies and Critic Reviews dataset, which includes 1,130,017 reviews with "fresh"/"rotten" ratings of 17,712 movies, of which 824,081 reviews contain subjective review scores (e.g. 3/5, B+, etc.). Our code for reproducible results can be found [here](https://github.com/jperelm/QTM350FinalProject/blob/main/Final%20Project.ipynb) and our blog post explaining our analysis can be found [here](http://ricottablogpost.s3-website-us-east-1.amazonaws.com/).

### Steps to replicate analysis with AWS

#### 1. [Set Up an AWS Account and Create an Administrator User](https://docs.aws.amazon.com/comprehend/latest/dg/setting-up.html) 
#### 2. [Store data in S3 bucket in AWS](https://docs.aws.amazon.com/AmazonS3/latest/userguide/creating-buckets-s3.html)
#### 3. [Process Movie reivews uisng AWS Comprehend](https://docs.aws.amazon.com/comprehend/latest/dg/getting-started.html)
        We can process the data to extract key phrasesand sentiment for later analysis. 
#### 4. [Analyze and Dipslay data using python (boto3)](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)

Overall, we found the [developer guide](https://docs.aws.amazon.com/comprehend/latest/dg/comprehend-dg.pdf) incredibly helpful for working with Amazon Comprehend.
