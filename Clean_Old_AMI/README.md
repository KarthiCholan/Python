# Python program to clean old AMI  based certain criteria such as age, tags


Cleaning by Age:
Listing AMIs: Use describe_images to retrieve a list of AMIs along with their creation dates.
Filtering by Age: Compare the creation date of each AMI with the desired threshold.
Deregistering AMIs: Use deregister_image to remove the AMIs that match the criteria.


Cleaning by Tags:
Listing AMIs with Tags: Retrieve AMIs and filter them based on specific tags.
Deregistering AMIs: Use deregister_image to remove the AMIs that match the specified tag criteria.
