# Python Program for Github-JIRA intergration Project 

Imports: The code starts by importing necessary modules:

requests: Used for making HTTP requests.
HTTPBasicAuth from requests.auth: For handling HTTP basic authentication.
json: For handling JSON data.
Flask: A web framework used here to create a web application.
Flask setup:

app = Flask(__name__): Creates a Flask application.
Route definition:

@app.route('/createJira', methods=['POST']): Defines a route /createJira that accepts POST requests.
createJira function:

This function is executed when the defined route receives a POST request.
It prepares the necessary data and sends a POST request to the Jira API to create an issue.
Jira API request:

It constructs the payload (JSON data) representing the issue to be created in Jira. The JSON structure includes information such as description, project key, issue type, and summary.
The requests.request() method sends an HTTP POST request to the Jira REST API using the provided URL, payload (converted to JSON), headers, and authentication information.
The response from the API call is then returned as a JSON-formatted string.
Running the Flask app:

if __name__ == '__main__': ensures that the Flask app runs only if this script is executed directly.
app.run(host='0.0.0.0', port=5000): Starts the Flask development server on host 0.0.0.0 and port 5000.
