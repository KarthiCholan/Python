# # Program to demonstrate integration with GitHub to fetch the 
# details of Users who created Pull requests(Active) on Kubernetes Github repo.


Importing Requests Library:

The script uses the requests library to send HTTP requests to the GitHub API.
GitHub API URL:

Defines the URL (url) to fetch pull requests from the Kubernetes GitHub repository (https://api.github.com/repos/kubernetes/kubernetes/pulls).

GET Request:

Sends a GET request to the GitHub API using requests.get(url) to retrieve data about the pull requests.
Note: Authentication headers can be added to this request for accessing private repositories or increasing rate limits.

Processing the Response:

Checks if the response status code is 200 (indicating a successful response).
If successful, converts the JSON response to a dictionary (pull_requests).
Creates an empty dictionary (pr_creators) to store the count of pull requests created by each user.

Iterating Through Pull Requests:

Loops through each pull request in the retrieved data.
Extracts the creator's username from each pull request and tallies the count of their pull requests in the pr_creators dictionary.

Displaying Results:

Prints the dictionary containing the usernames of PR creators along with the count of pull requests they've created.
