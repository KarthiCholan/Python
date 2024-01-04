# Python script to list files in folders


list_files_in_folder Function:

Accepts a folder_path as input.
Attempts to list the files in the specified folder using os.listdir(folder_path).
If successful, returns a tuple containing the list of files (files) and None for the error message.
Catches specific exceptions like FileNotFoundError and PermissionError, returning None for files and a relevant error message for the encountered issue.

main Function:

Requests the user to input a list of folder paths separated by spaces.
Splits the input into a list of folder paths (folder_paths).
Iterates through each folder path in folder_paths.
Calls list_files_in_folder for each folder path to retrieve the files or error messages.
If files are found, it prints the list of files in each folder. Otherwise, it displays the error message.

Usage:

Upon execution, the script prompts the user to enter folder paths separated by spaces.
It then displays the files within each specified folder path or error messages in case of issues like folder not found or permission denied.

