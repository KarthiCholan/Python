# AWS Lambda functions to start and stop EC2 instances 

1. Create IAM Role for Lambda
Create an IAM role that provides necessary permissions to start and stop EC2 instances. Attach policies like AmazonEC2FullAccess (for demonstration purposes) or create a custom policy with more restricted permissions.

2. Write Lambda Functions
3. Set Up AWS EventBridge to Trigger Lambda Functions
Start EC2 Instances:
Go to the AWS EventBridge  console.
Click on "Create rule".
Under "Event Source", select "Schedule".
Choose fixed rate or cron expression as the schedule to trigger the Lambda function.
For the target, select "Lambda function" and choose the Lambda function you created for starting instances.
Save the rule.

Stop EC2 Instances:
Follow similar steps as above but create a separate AWS EventBridge Rule to trigger the Lambda function responsible for stopping instances.
