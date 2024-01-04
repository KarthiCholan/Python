# Backing up files to Amazon S3 using Boto3 

Importing boto3 and os:

Imports the boto3 library for AWS interactions and the os module for handling local file operations.

Initializing the S3 Client:

Initializes the Amazon S3 client using boto3.client('s3').

backup_to_s3 Function:

Accepts the local folder path (local_folder) containing the files to be backed up and the name of the S3 bucket (bucket_name).
Retrieves a list of files in the local folder using os.listdir(local_folder).
Iterates through each file and constructs the S3 file key/path as backup/{file_name}.
Uses s3.upload_file() to upload each file from the local folder to the specified S3 bucket with the specified S3 file key.
Prints a message for each file upload to provide feedback.

Setting Local Folder Path and S3 Bucket Name:

Sets the local_backup_folder variable with the local folder path containing the files to be backed up.
Sets the s3_bucket_name variable with the name of the target S3 bucket.

Calling the backup_to_s3 Function:

Calls the backup_to_s3 function with the specified local folder path and S3 bucket name.
