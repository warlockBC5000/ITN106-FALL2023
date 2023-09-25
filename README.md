#ITN106-FALL2023

# Windows Command Prompt Tutorial

The Windows Command Prompt is a powerful tool for managing and interacting with your computer through text-based commands. In this tutorial, we will cover the basics of using the Command Prompt, including navigation, file management, and some useful commands.

## Table of Contents
1. **Accessing the Command Prompt**
2. **Basic Navigation**
3. **Working with Files and Directories**
4. **Useful Commands**
   - `dir` (List Directory Contents)
   - `cd` (Change Directory)
   - `mkdir` (Create Directory)
   - `rmdir` (Remove Directory)
   - `copy` (Copy Files)
   - `move` (Move Files)
   - `del` (Delete Files)
   - `ipconfig` (View IP Configuration)
   - `ping` (Check Network Connectivity)
5. **Batch Scripting**

## 1. Accessing the Command Prompt
To open the Command Prompt:
- Press `Win + R`, type `cmd`, and press `Enter`.
- Search for "Command Prompt" or "cmd" in the Start menu.

## 2. Basic Navigation
- Use `cd` (Change Directory) to navigate between folders.
   ```
   cd [directory_path]
   ```

- Use `cd ..` to move up one level in the directory tree.
   ```
   cd ..
   ```

- Use `dir` to list the contents of the current directory.
   ```
   dir
   ```

## 3. Working with Files and Directories
- Use `mkdir` to create a new directory.
   ```
   mkdir NewFolder
   ```

- Use `rmdir` to remove a directory (must be empty).
   ```
   rmdir OldFolder
   ```

- Use `copy` to copy files.
   ```
   copy file.txt destination_folder
   ```

- Use `move` to move files.
   ```
   move file.txt destination_folder
   ```

- Use `del` to delete files.
   ```
   del file.txt
   ```

## 4. Useful Commands
### a. `ipconfig` (View IP Configuration)
- Displays information about your network adapters and their configurations.
   ```
   ipconfig
   ```

### b. `ping` (Check Network Connectivity)
- Tests network connectivity to a specific host or IP address.
   ```
   ping google.com
   ```

## 5. Batch Scripting
You can create batch scripts (`.bat` or `.cmd` files) to automate tasks using Command Prompt commands. Here's a simple example of a batch script that backs up files:

```batch
@echo off
rem This is a batch script to back up files.

rem Set the source and destination folders
set source_folder=C:\Source
set destination_folder=D:\Backup

rem Copy files from the source to the destination
xcopy "%source_folder%" "%destination_folder%" /E /I /Y

rem Display a message when done
echo Backup completed.

rem Pause to keep the window open
pause
```

Save this script with a `.bat` extension and run it by double-clicking. It will copy files from the source folder to the destination folder and display a message when finished.

That's it! You now have a basic understanding of the Windows Command Prompt. Experiment with these commands and explore more advanced features as you become more comfortable with the Command Prompt.
