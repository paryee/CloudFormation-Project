# CloudFormation-Project
Project: Hosting a JavaScript Application on AWS Using CloudFormation and a Serverless Service via AWS Console.
This project involves cloning and hosting a JavaScript application on AWS using the AWS Management Console. The infrastructure will be set up using a CloudFormation template, and the application will be deployed using AWS Lambda as a serverless hosting service.
Objective
1. Clone a simple JavaScript web application on https://github.com/paryee/CloudFormation-Project.
2. Use AWS CloudFormation to provision the infrastructure:
•
AWS Lambda (to serve static files via a custom API Gateway endpoint)
•
API Gateway (to expose the app to users)
3. Deploy the app using the AWS Lambda service through the AWS Console.
Guidance Steps.
Step 1: Clone the JavaScript Application from https://github.com/paryee/CloudFormation-Project.
Step 2: Prepare the ZIP File.
•
Package index.html, style.css and app.js into a ZIP file, as AWS Lambda requires code to be uploaded in this format.
Step 3: Create a CloudFormation Template.
The template should create:
•
An AWS Lambda function.
•
An API Gateway endpoint to serve the application.
Step 4: Deploy via AWS Console.
1. Upload the ZIP to S3:
•
Go to the S3 Console.
•
Create a bucket (with the application name).
•
Upload the todo-app.zip file.
2. Launch CloudFormation Stack:
•
Go to the CloudFormation Console.
•
Click Create Stack > With New Resources (Standard).
•
Upload the template.yaml file.
•
Replace <Replace-With-Your-S3-Bucket-Name> in the template with the actual bucket name.
•
Follow the prompts to launch the stack.
3. Verify API Gateway Endpoint:
Once the stack is created, navigate to the *API Gateway Console*.
•
Find the API created.
•
Deploy the API to a stage (e.g., prod).
•
Copy the endpoint URL (e.g., https://<api-id>.execute-api.<region>.amazonaws.com/prod/app).
4. Test the App:
•
Paste the endpoint URL into your browser. If everything is set up correctly, your app will load.
Step 5: Optional Enhancements (Extra Points).
Add Monitoring:
•
Enable AWS CloudWatch logs for the Lambda function.
Add Caching:
•
Use API Gateway caching to improve performance.
Add Security:
•
Use an AWS WAF (Web Application Firewall) to protect the API Gateway.
Submission
•
Push all files (Javascript app files and cloudformation template) into your personal GitHub account to boost your portfolio.
