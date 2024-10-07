# Auto Shutdown Batch File for Missing Folder

## Overview
This batch file script is designed to check for the existence of a folder named `itsme` on the user's desktop within 10 seconds after system startup. If the folder is not found, the computer will automatically shut down. This can be particularly useful in scenarios where certain critical folders need to be present on the desktop to ensure proper workflow.

## Features
- Automatically checks for the presence of the specified folder.
- Initiates an automatic shutdown if the folder is missing.
- Simple and easy to use for Windows users.

## Usage Instructions
1. **Create a New File**:
   - Open Notepad or any text editor and copy the code below into the file:

   ```batch
   @echo off
   set desktopPath=%USERPROFILE%\Desktop
   timeout /t 10 /nobreak >nul
   if not exist "%desktopPath%\itsme" (
       shutdown /s /f /t 0
   )

#Save the File:

Save the file with a .bat extension, for example, checkFolder.bat.
Add to Startup:

Place the .bat file in the Windows startup folder to ensure it runs automatically after startup.
Testing:

To test the script, create a folder named itsme on your desktop. If the folder is present, the script will do nothing; if it is absent, the computer will shut down after 10 seconds.
Important Notes
Caution: Use this script carefully, as it will force the computer to shut down if the specified folder does not exist. Ensure that you create the itsme folder on your desktop before running the script to avoid unexpected shutdowns.
This script is intended for personal use and should be tested in a safe environment.
Contributing
If you would like to contribute to this project, please feel free to fork the repository and submit a pull request.
