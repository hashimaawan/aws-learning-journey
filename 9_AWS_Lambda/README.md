# AWS Lambda
AWS Lambda is a serverless compute service that lets you run code without provisioning or managing servers. 

- Pay only for execution time (per 1ms).
- Automatically scales based on request volume.
- Can be triggered by many AWS services or external APIs.

## EC2 vs AWS Lambda

Belongs to same family as ec2. Unlike EC2, Lambda charges only for active compute time and the number of requests made. In ec2 you ahve to set the different parameters for compute like intance id, etc but in lambda, it automatically creates the server and once operation performed it automatically tears down the server and saving cost.
ec2 --> Ip address
lambda --> no hosted, ip address info


## Prerequisites

**Before you start:**
AWS Account (free tier works fine)

AWS CLI installed (aws configure)

Basic knowledge of Python or Node.js

IAM user with permissions: AWSLambdaFullAccess, AmazonS3FullAccess, AmazonAPIGatewayInvokeFullAccess