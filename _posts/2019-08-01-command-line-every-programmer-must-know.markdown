---
date: 2019-08-01T08:18:58.000Z
layout: post
title: Command Line Every Programmer Must Know
subtitle: Mastering the command line is a must for every programmer.
description: Mastering the command line is a must for every programmer.
image: /assets/images/post_images/command-line.jpeg
optimized_image: /assets/images/post_images/command-line.jpeg
category: Python
tags:
  - Coding
  - Tools
author: sarthakgarg
paginate: true
---
Interacting with a computer through a command-line interface (CLI) is a powerful technique. Mastering the command line can greatly improve your productivity during development. The best way to do this is to keep a list of selected commands ready for a quick glance whenever you get stuck. 

Below is a curated list of the most fundamental commands. Would suggest to bookmark this post.

### STARTER

* Find out the language of the terminal (zsh/bash/sh): `echo $0`
* Print the current path: `echo $PATH`
* Read manual of a command: `man <cmd>` (\[ENTER] to scroll, q to quit)
* Add sudo automatically to the last command: `sudo !!`
* Give your own name to a command: `alias cls=clear` (Alias for a sequence of command to be wrapped in quotes. To make alias permanent, add the commands in .zshrc)
* Change the password of a user: `sudo passwd <username>`
* Ping the server: `ping <URL>`
* Simple text editor: `nano`

### SYSTEM INFO AND SETUP
* Linux System Information: `uname -a` (use `w` to see current logged-in users)
* Real-time status of system processes: `top` (you can use `ps` also for listing current processes)
* Kill a process by specifying its PID: `kill`
* Exit (terminate) any current process and start a new line: `^c` (^ = \[CTRL])
* Manage System Settings: `sudo systemsetup`
* Report System Hardware and Software Configurations: `system_profiler`
* System Security Frameworks: `security`
* Manage system configuration parameters: `scutil --help` (Ex. `scutil --get HostName`, `sudo scutil --set HostName <Host_Name>`)
* Set an environment variable: `env` (you can also use `export`)

### WORKING WITH DIRECTORIES

* Print the working directory: `pwd`
* Go back to a directory: `cd ..`
* Go two directories back: `cd ../..`
* Go to Root directory: `cd /`
* Go to Home directory: `cd [ENTER]`
* Create a directory: `mkdir <dir_name>`
* Create multiple directories: `mkdir <dir1> <dir2> <dirN>`
* Remove dir: `rm -rf <dir_name>` (r - recursive, f - force)

### WORKING WITH FILES

* View files in directory view with details: `ls -1` (use -lt or add -t to sort, -a to list hidden files)
* View files with a specific file extension: `ls *<.extn>`
* List the files in a specific directory: `ls <dir_name>`
* Create a file: `touch <file_name>`
* Create a file in a directory using echo: `echo "<text>" > <file_name>`
* Copy file: `cp <copy_file> <copied_file>`
* Rename file: `mv <file_name> <new_name>`
* Move file: `mv <file_name> <dir_path>`
* Remote file copy: `rsync SOURCE DESTINATION`
* Read a file: `cat <file_name> | less` (Lists the contents of files to the terminal window, faster than Open. Less allows to use up & down keys. Type q to quit from less.)
* Print first few lines of a file: `head example.txt` ('use -n <no_of_lines>, default is 10. use `tail` for printing last lines.)
* Open a file: `open <file_path>`
* Remove file: `rm <fine_name>` (this will remove file not dir)
* Securely remove files or directories: `srm <file_name>`
* Write to a file: `echo "<text>" >> <file_name>` (use > to rewrite the text)
* Search: `grep <search_string> <file_name>` (grep can search in multiple files, use wildcard *.<file_extn> instead file name.)
* Print text of multiple files together: `cat <file1> <file2>`
* Concatenate content of multiple files: `cat <file1> <file2> > <file3>`
* Merge two files with output to outfile: `sdiff -o outfile from-file to-file`
* To set file permissions: `chmod -R 765 example.txt` (Digits seq for Owner, Groups, & Others. Permissions: 0-No permission; 1-Execute(x); 2-Write(w); 3-Write and execute; 4-Read(r); 5-Read and execute; 6-Read and write; 7-Read, write and execute
* Compress a file: `gzip -k example.txt`
* Display file details: `stat <file_name>` 
* List the metadata attributes for a specified file: `mdls <file_name>`

### VIRTUAL ENV

* Create a new virtual environment: `python -m venv <dir_name>`
* Goto `<dir_name>/bin` and activate: `source activate` (This will prepend the path to “venv” at the beginning of the $PATH variable)
* Exit the virtual environment: `deactivate`

### PYTHON

* Open Python terminal: `python`
* Execute a command: `python -c "print('Real Python')"`
* Exit Python terminal: `>>> exit()` (or \\[CRTL]D)
* Map Python Version (Mac ZSH): `echo "alias python=/usr/local/bin/python3.7" >> ~/.zshrc`

### PIP

* Pip install package: `pip install <package-name>`
* Install specific development version from Github: `python3 -m pip install git+<git_URL>`
* Pip upgrade package: `pip install --upgrade <package-name>`
* Force install a version if you've already installed: `python3 -m pip install --force-reinstall git+<git_URL>`
* Pip uninstall package: `pip uninstall <package-name>`

### JUYPTER LAB (Optional)

* Start JupyterLab: `jupyter lab`

### RASA (Optional)

* Create new project: `rasa init --no-prompt`
* Train model: `rasa train`
* Talk to assistant: `rasa shell`

### ULTIMATE TRICKS

* Youtube video download: `youtube-dl <URL>` (1. install [youtube-dl](https://github.com/ytdl-org/youtube-dl). use `-F` to list available formats, `-f <format_code1>+<format_code..n>` to download specific formats.)
* Download file from internet: `curl -s <URL> > <file_name>` (-s to see the download progress, you can use -o (output) option for saving the file)
* Capture an image of the whole or part of the screen: `screencapture -i -p` (for other options, refer `man screencapture`)
* Convert text to audible speech: `cat myfile.txt | say` (for other options, refer `man say`)
* Prevent the system from sleeping: `caffeinate -u -t 3600` (caffeinate for 1 hour)
