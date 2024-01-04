# Steps to configure to trigger SNS Notification when EC2 stops using AWS Lambda and AWS EventBridge
1. Create an SNS Topic
Go to the Amazon SNS console.
Click "Create topic" and provide a name and a display name.
Once created, note the ARN (Amazon Resource Name) of the SNS topic.
2. Create an IAM Role for Lambda
Create an IAM role that grants the Lambda function permission to publish messages to your SNS topic.

3. Write Lambda Function
Write a Lambda function that will be triggered by the AWS Eventbridge when an EC2 instance changes state to 'stopped'.

4. Configure AWS Event Bridge Rule
Go to the Amazon CloudWatch console.
Click on "Create rule".
Under "Event Source", select "Event Pattern".
Choose "EC2" as the service name, "EC2 Instance State-change Notification" as the Event type.
Define the specific state change(s) you want to trigger the Lambda function (e.g., 'Stopped').
For the target, select "Lambda function" and choose the Lambda function you created earlier.
Save the rule.



![image](https://github.com/KarthiCholan/Python/assets/108706606/676f61a7-55e1-4826-8242-ad706759fbdb)
