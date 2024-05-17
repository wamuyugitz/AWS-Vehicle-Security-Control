# AWS-Vehicle-Security-Control

The project aims to demonstrate proficiency in cloud application development on the AWS platform by implementing an application for Label and Text Detection of image files using AWS Rekognition AI services. It consists of five parts:

<img width="433" alt="image" src="https://github.com/wamuyugitz/AWS-Vehicle-Security-Control/assets/100859393/b758fa39-d0e6-4b00-ae0e-f09f4a1339ae">


1. Resource creation with Boto3 and CloudFormation: Using Python (Boto3), an EC2 instance and an S3 bucket are created, along with an SQS queue and a DynamoDB table via CloudFormation template.

2. Image file upload to S3 and Lambda trigger from SQS: A Python application running on the EC2 instance uploads provided image files to the S3 bucket at intervals, triggering a Lambda function through an SQS queue.

3. Label and Text Detection with AWS Rekognition: A Lambda function written in Python (Boto3) extracts image file details from the SQS message and utilizes AWS Rekognition to detect vehicle labels and plate numbers.

4. Database Update and Email Notification: Relevant information from the Label and Text detection response is saved to a DynamoDB table. The Lambda function compares vehicle details with a whitelist/blacklist and sends email notifications to a security officer for blacklisted vehicles or when no records are found.
