# AWS Three-Tier Architecture

This project is a straightforward website designed for claiming complimentary gifts by capturing the user's name as input and checking for previous claims. The Lambda function validates the input against DynamoDB; if absent, it stores the information. Moreover, upon each successful claim, the Lambda function queries a generative AI model in AWS Bedrock, returning a celebrity name sharing the same first name as the user.

Implemented with an AWS three-tier architecture, the project leverages essential services such as Amplify, API Gateway, Lambda, IAM, and DynamoDB. Amplify serves as the presentation layer by hosting the static website, while API Gateway and Lambda handle the application logic, and DynamoDB acts as the database layer. Security is ensured through the integration of IAM roles with these services.

In addition to the Amplify frontend, the project explores two alternative variants. The first employs S3 for hosting a static website as the frontend, while the second utilizes an EC2 instance to retrieve the HTML file from an S3 bucket and host an Apache Web server as the frontend.
