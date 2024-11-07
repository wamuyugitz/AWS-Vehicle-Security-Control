# AWS-Vehicle-Security-Control

This project is a vehicle control system developed for a security entrance, leveraging AWS cloud services to detect vehicles and recognize license plates in images. The application was developed for the Cloud Platform Development module using the AWS Rekognition service for AI-based image recognition.

## Project Objectives
The system performs several automated tasks to ensure security and control access:
- Detect vehicle labels and license plates in images.
- Store vehicle data in a secure and efficient way.
- Alert security personnel if unauthorized vehicles are detected.
  
<img width="433" alt="image" src="https://github.com/wamuyugitz/AWS-Vehicle-Security-Control/assets/100859393/b758fa39-d0e6-4b00-ae0e-f09f4a1339ae">

## Architecture

The project architecture consists of the following AWS services:
1. **EC2 Instance**: Acts as the simulated camera system, uploading images to S3 at 30-second intervals.
2. **S3 Bucket**: Stores vehicle images for processing.
3. **SQS Queue**: Triggers the Lambda function to process new images.
4. **Lambda Function**: Detects and extracts vehicle labels and text (license plate numbers) from images using AWS Rekognition.
5. **DynamoDB**: Stores vehicle data and tracks whether a vehicle is authorized.
6. **Email Notification**: Alerts security if an unauthorized vehicle is detected.
