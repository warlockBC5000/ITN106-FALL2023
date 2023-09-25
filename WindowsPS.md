# Windows PowerShell Tutorial

PowerShell is a robust command-line shell and scripting language that's built into Windows. It offers more capabilities and flexibility than the standard Command Prompt. In this tutorial, we will cover the fundamentals of Windows PowerShell, including navigation, basic commands, scripting, and examples.

## Table of Contents
1. **Accessing PowerShell**
2. **Basic Navigation**
3. **Working with Commands**
4. **Variables and Data Types**
5. **Scripting Basics**
6. **Examples**

## 1. Accessing PowerShell
To open PowerShell:
- Press `Win + X` and choose "Windows PowerShell" or "Windows PowerShell (Admin)".
- Search for "PowerShell" in the Start menu.

## 2. Basic Navigation
- Use `cd` (Change-Location) to navigate between folders.
   ```powershell
   cd [directory_path]
   ```

- Use `cd ..` to move up one level in the directory tree.
   ```powershell
   cd ..
   ```

- Use `Get-ChildItem` (or `dir` for short) to list the contents of the current directory.
   ```powershell
   Get-ChildItem
   ```

## 3. Working with Commands
- Use `Get-Help` to get help for a command.
   ```powershell
   Get-Help Get-Process
   ```

- Use `Get-Command` to list all available commands.
   ```powershell
   Get-Command
   ```

- Use `Invoke-Expression` to run a command stored in a string.
   ```powershell
   $command = "Get-Process"
   Invoke-Expression $command
   ```

## 4. Variables and Data Types
- Use `$variable_name` to create and access variables.
   ```powershell
   $name = "John"
   Write-Host "Hello, $name!"
   ```

- PowerShell supports various data types, including strings, integers, arrays, and more.

## 5. Scripting Basics
You can create PowerShell scripts (`.ps1` files) to automate tasks. Here's a simple example of a script that lists running processes:

```powershell
# This is a PowerShell script to list running processes.

# Get a list of processes
$processes = Get-Process

# Display the list
foreach ($process in $processes) {
    Write-Host "Process Name: $($process.Name), ID: $($process.Id)"
}
```

Save this script with a `.ps1` extension and run it using PowerShell.

## 6. Examples
### a. File Backup Script
Here's an example of a PowerShell script that backs up files:

```powershell
# This is a PowerShell script to back up files.

# Set the source and destination folders
$sourceFolder = "C:\Source"
$destinationFolder = "D:\Backup"

# Copy files from the source to the destination
Copy-Item -Path $sourceFolder -Destination $destinationFolder -Recurse -Force

Write-Host "Backup completed."
```

### b. Service Management
You can use PowerShell to start or stop services. For example, to stop the Print Spooler service:

```powershell
# Stop the Print Spooler service
Stop-Service -Name "Spooler"
```

This tutorial covers the basics of Windows PowerShell. As you become more familiar with it, you can explore more advanced features, modules, and scripting techniques to streamline your administrative tasks and automation efforts.
