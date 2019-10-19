# datapipeline-python
Projects of building data pipelines with python scripts

### excel_csv_to_s3.py 

This file is python script for modifying existing excel xlsx worksheets, converting them to csv formats, and upload them to AWS S3.

With regards to modifying the existing files, in this application there were a series of historic excel files having the same template but different values over time. It required to add a new column to hold new generated primary ID's to differntiate the data from different time.

The modified excel files were then converted to csv format and saved to a local directory (as a reference), and uploaded to AWS S3 with Boto3 API.

### lambda_s3_csv_dynamo.py 

This is a lambda function in python for loading the csv files to AWS DynamoDB once they are uploaded from local directory to AWS S3. For any updates (incremental changes) made to the csv files in S3, the lambda function will also made the updates available in the DynamoDB table very quickly. 

