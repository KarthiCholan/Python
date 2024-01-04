# Python program to list EC2 instances and Status across all regions in an AWS account

Importing the boto3 Library:

boto3: The AWS SDK for Python.
EC2 Client Initialization:

ec2_client = boto3.client('ec2'): Creates an EC2 client.
Retrieving All Regions:

regions: Retrieves a list of all available regions using ec2_client.describe_regions()['Regions'].
The list comprehension extracts the region names from the response.
Looping Through Regions:

Iterates through each region in the regions list.
Creates an ec2 resource object for the specific region using boto3.resource('ec2', region_name=region).
Retrieves instances in the region using instances = ec2.instances.filter().
Loops through the instances and prints their IDs and status.
