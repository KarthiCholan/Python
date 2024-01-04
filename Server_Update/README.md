# Python program to  update a server configuration file by modifying the value associated with a specified key.



update_server_config Function:

Accepts three parameters:
file_path: Path to the server configuration file.
key: The key whose value needs to be updated.
value: The new value to be set for the specified key.

Reading Existing Configuration:

Opens the server configuration file in read mode ('r') and reads all its lines into the lines variable.

Updating Configuration:

Opens the same file in write mode ('w') to update its content.
Iterates through each line in the lines.
Checks if the key is present in each line:
If the line contains the specified key, it replaces the line with a new line containing the key and the provided value.
If the line doesn't contain the specified key, it writes the line as it is to the file.

Usage:

Defines the server_config_file variable with the path to the server configuration file ('server.conf' in this case).
Specifies the key_to_update variable, which identifies the configuration key to be updated ('MAX_CONNECTIONS').
Sets the new_value variable with the new value to be assigned to the specified key ('600' in this case).
Calls the update_server_config function to perform the update.
