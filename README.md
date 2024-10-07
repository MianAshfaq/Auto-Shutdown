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
