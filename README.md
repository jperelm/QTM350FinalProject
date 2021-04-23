# QTM350 Final Project-Ricotta e Spinaci
This is our team's work for the final project for QTM 350 (Spring '21)

By: Laura Neff, Jason Hamilton, Jason Perelman, and Chris Nicholson

In this project, we will collect written movie reviews, perform sentiment analysis using [AWS Comprehend](https://aws.amazon.com/comprehend/), and then analyze Comprehend's accuracy using a variety of statistical techniques. We will be using two different corpora of movie reviews specifically designed for sentiment analysis projects: 1) the Cornell Movie Reviews Database, which includes 5,006 movie reviews and ratings (0-1) by four different authors, and 2) the Rotten Tomatoes Movies and Critic Reviews dataset, which includes 1,130,017 reviews with "fresh"/"rotten" ratings of 17,712 movies, of which 824,081 reviews contain subjective review scores (e.g. 3/5, B+, etc.). Our code for reproducible results can be found [here](https://github.com/jperelm/QTM350FinalProject/blob/main/Project_reviews.ipynb) and our also check out our [blog post explaining our analysis](http://ricottablogpost.s3-website-us-east-1.amazonaws.com/).

### Steps to replicate analysis with AWS

#### 1. [Set Up an AWS Account](https://docs.aws.amazon.com/comprehend/latest/dg/setting-up.html)
#### 2. [Create a SageMaker Notebook Instance](https://docs.aws.amazon.com/sagemaker/latest/dg/howitworks-create-ws.html)
#### 3. Grant Permissions to SageMaker to Access Amazon Comprehend and S3
After creating a SageMaker notebook, first, navigate to the AWS Management Console and click on IAM to open the IAM dashboard:

![aws console](https://github.com/jperelm/QTM350FinalProject/blob/main/screenshots/awsconsole.png)

Next, from the IAM dashboard, click on "Roles":

![iam dash](https://github.com/jperelm/QTM350FinalProject/blob/main/screenshots/iamdash.png)

From the IAM roles page, click on the IAM role which matches the one which you used when setting up the SageMaker notebook:

![iam roles](https://github.com/jperelm/QTM350FinalProject/blob/main/screenshots/iamroles.png)

After clicking on the SageMaker IAM role, you will see a tab for "Permissions" which allows you to assign specific resources you allow the SageMaker notebook instance to access on AWS. Add the "AmazonS3FullAccess", "ComprehendFullAccess", and "AmazonSageMakerFullAccess" permissions (if not already added) to this IAM role by clicking on the "Attach policies" button and searching for the name of the specific permission:

![sagemaker permissions](https://github.com/jperelm/QTM350FinalProject/blob/main/screenshots/sagemakerperms.png)

#### 4. Clone this repository in SageMaker
First, open a SageMaker notebook instance in AWS. You can either create a new terminal window and paste the following commands:

<pre>cd /root/  
git clone git@github.com:jperelm/QTM350FinalProject.git</pre>

Alternatively, you may download the zip file of the master branch of this repository to your local machine and upload it via JupyterLab, by clicking on the upload button (highlighted below) in your SageMaker notebook instance:

![sagemaker upload](https://github.com/jperelm/QTM350FinalProject/blob/main/screenshots/empty_notebook.png) 

Overall, we found the [developer guide](https://docs.aws.amazon.com/comprehend/latest/dg/comprehend-dg.pdf) incredibly helpful for working with Amazon Comprehend in SageMaker notebooks.
