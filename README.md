# Project 1: Linux & Command Line Basics

## DevOps Industrial Training

**Author:** DevOps Intern
**Domain:** DevOps Engineering
**Batch:** 2026
**Status:** Completed & Verified

---

## Project Overview

This project demonstrates basic Linux command-line operations used in a DevOps environment.

The complete project was performed through the Linux terminal without using a Graphical User Interface (GUI).

The main purpose of this project was to practice creating directories and files, managing log files, checking file information, and verifying the final directory structure.

---

## Objectives

The main objectives of this project were:

* Create directories using Linux commands.
* Create configuration files.
* Add information to a log file.
* Inspect directories and files recursively.
* Rename a log file for backup purposes.
* Check file permissions and ownership.
* Verify the final project structure.
* Become familiar with basic Linux commands used in DevOps.

---

## Project Structure

The project created the following structure:

```text
/app
├── config.conf
└── logs
    └── server.bak
```

The original `server.log` file was renamed to `server.bak` as part of the log archival step.

---

## Step-by-Step Implementation

### 1. Create Directories

The required application and logging directories were created using `mkdir`.

```bash
sudo mkdir -p /app/logs
```

### Explanation

The `mkdir` command is used to create directories.

The `-p` option allows the complete directory path to be created at once. In this case, it creates:

```text
/app
/app/logs
```

---

### 2. Create Configuration File

An empty configuration file was created using the `touch` command.

```bash
sudo touch /app/config.conf
```

### Explanation

The `touch` command can be used to create a new empty file.

The file created in this step was:

```text
/app/config.conf
```

---

### 3. Add Log Entry

An initial status message was added to the server log file.

```bash
echo "Started" | sudo tee /app/logs/server.log
```

### Explanation

The `echo` command generates the text:

```text
Started
```

The pipe symbol `|` sends this output to the `tee` command.

The `tee` command writes the output into:

```text
/app/logs/server.log
```

This created the initial server log file.

---

### 4. Check Directory Structure

The working directory and complete `/app` directory structure were checked.

```bash
pwd && sudo ls -R /app
```

### Explanation

`pwd` displays the current working directory.

`ls -R /app` lists the contents of `/app` recursively, including its subdirectories and files.

The `&&` operator allows the second command to run after the first command completes successfully.

---

### 5. Rename Log File

The server log file was renamed as a backup file.

```bash
sudo mv /app/logs/server.log /app/logs/server.bak
```

### Explanation

The `mv` command is commonly used to move or rename files.

In this project, it was used to rename:

```text
server.log
```

to:

```text
server.bak
```

This represents a simple log backup or archival operation.

---

### 6. Check File Permissions

The configuration file information was inspected.

```bash
sudo ls -l /app/config.conf
```

### Explanation

The `ls -l` command provides detailed information about a file, including:

* File permissions
* File owner
* Group
* File size
* Date and time information
* File name

This was useful for performing a basic security and permission check.

---

### 7. Verify Final Directory Structure

The final state of the project was checked using:

```bash
sudo ls -R /app
```

### Explanation

This command recursively displays the complete `/app` directory structure.

It was used to confirm that the required files and directories were created successfully and that the log file had been renamed.

---

## Commands Used

The main Linux commands used in this project were:

| Command    | Purpose                                         |
| ---------- | ----------------------------------------------- |
| `mkdir -p` | Create directories and parent directories       |
| `touch`    | Create an empty file                            |
| `echo`     | Display or generate text                        |
| `tee`      | Write command output to a file                  |
| `pwd`      | Display the current working directory           |
| `ls -R`    | List directories and files recursively          |
| `ls -l`    | Display detailed file information               |
| `mv`       | Move or rename files                            |
| `sudo`     | Execute commands with administrative privileges |

---

## What I Learned

Through this project, I learned how to:

* Work with the Linux command line.
* Create directory structures using `mkdir`.
* Create files using `touch`.
* Write log information using `echo` and `tee`.
* Inspect directories recursively.
* Rename files using `mv`.
* Check file permissions and ownership.
* Perform basic Linux system administration tasks.

---

## Conclusion

This project provided practical experience with basic Linux command-line operations. It helped me understand how files and directories can be created, managed, inspected, and organized using terminal commands.

These commands are commonly used in DevOps environments for basic server administration and file management.

