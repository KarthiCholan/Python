# Python program to find and delete X Days old files

get_files_older_than_days Function:

Accepts a folder_path and a days parameter.
Calculates the current date (current_date) using datetime.datetime.now().
Calculates a threshold_date by subtracting days from the current_date.
Walks through the directory tree using os.walk(folder_path) and checks each file's modification time.
Files with modification times earlier than threshold_date are added to the older_files list.
Returns the list of files older than the specified number of days.

delete_files Function:

Accepts a list of file paths (files) as input.
If no files are provided, it prints a message and returns.
If there are files to delete, it lists them and asks for confirmation.
If the user confirms deletion by entering "yes," it proceeds to delete each file using os.remove(file).
If the user enters anything other than "yes," it aborts the deletion.

Main Execution:

Asks the user to input the folder path and the number of days.
Calls get_files_older_than_days with the provided inputs to get the list of older files.
Passes the list of older files to delete_files for potential deletion.
