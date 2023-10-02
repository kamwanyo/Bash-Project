# File Permissions Manager Script

This script is a simple file permissions manager for Unix-like operating systems. It allows you to view and modify the ownership and access permissions of a file or directory.

## Features

- **Argument Handling**: The script takes a filename or directory name as an argument. If no argument is provided, it displays usage information and exits.

- **Option Handling**: The script includes a `-h` option that can be used to display information on how to use the script.

- **Error Handling**: The script handles invalid options and arguments with appropriate error messages.

- **File/Directory Existence Check**: The script checks if the provided file or directory exists before proceeding.

- **Ownership and Permissions Display**: The script displays the current ownership and permissions of the file or directory.

- **Ownership Modification**: The script asks if you want to change the owner of the file or directory. If you answer 'y' (either uppercase or lowercase), it prompts you to enter the new owner name and changes the owner using the `chown` command.

- **Group Modification**: Similarly, the script asks if you want to change the group of the file or directory. If you answer 'y', it prompts you to enter the new group name and changes the group using the `chgrp` command.

- **Access Permissions Modification**: The script also asks if you want to change the access permissions of the file or directory. If you answer 'y', it prompts you to enter the new access permissions in octal format (e.g., 755). It uses a regular expression to validate that the entered permissions are in a valid octal format. If an invalid mode is entered, it displays an error message and terminates execution. If a valid mode is entered, it changes the access permissions using the `chmod` command.

- **Updated Ownership and Permissions Display**: After any modifications, the script displays the updated ownership and permissions of the file or directory.

## Usage

To use this script, navigate to its location in your terminal and run it with a filename or directory name as an argument, like so:

```bash
./Yowano_Project filename
```

Replace `filename` with the name of your file or directory. You can also use a relative or absolute path if necessary.

To display usage information, run the script with the `-h` option:

```bash
./Yowano_Project -h
```

Please note that changing ownership and permissions typically requires superuser privileges, so you may need to run this script with `sudo` depending on your system's security settings.
