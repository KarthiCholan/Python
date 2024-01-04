# Python program to automate EC2 AMI (Amazon Machine Image) backups

Importing Libraries:

boto3: The AWS SDK for Python.
AWS Configuration:

aws_access_key, aws_secret_key, aws_region: Variables storing your AWS access key, secret key, and the region where your instances reside.
EC2 Client Initialization:

ec2_client: Initialization of the EC2 client using the provided access key, secret key, and region.
create_ami Function:

create_ami(instance_id): This function creates an AMI of the specified EC2 instance.
It generates a timestamp for the AMI name to make it unique, and then uses ec2_client.create_image() to create the AMI. Optionally, it allows you to specify whether to reboot the instance during AMI creation (NoReboot=True in this case).

list_instances Function:

list_instances(): This function retrieves a list of all EC2 instance IDs in your AWS account.
It uses ec2_client.describe_instances() to get information about instances and extracts their IDs.

Instances to Backup:

instances_to_backup: A list containing the instance IDs for which you want to create AMIs. Replace 'INSTANCE_ID_1' and 'INSTANCE_ID_2' with your actual instance IDs.

Creating AMIs:

A loop iterates over the instances_to_backup list.
For each instance ID, it calls create_ami() to create an AMI and prints a message indicating the creation of the AMI for that instance.
