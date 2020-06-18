---
date: 2020-02-01T08:18:58.000Z
layout: post
title: Command Line Basics
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

#### LINUX TERMINAL

* Read manual of a command: `$ man <cmd>` (\[ENTER] to scroll, q to quit)
* Find out the language of the terminal (zsh/bash/sh): `$ echo $0`
* Exit (terminate) any current process and start a new line: `$ ^c` (^ = \[CTRL])
* Map Python Version (Mac ZSH): `$ echo "alias python=/usr/local/bin/python3.7" >> ~/.zshrc`

#### VIRTUAL ENV

* Create a new virtual environment: `$ python -m venv <dir_name>`
* Goto `<dir_name>/bin` and activate: `$ source activate` (This will prepend the path to “venv” at the beginning of the $PATH variable)
* Exit the virtual environment: `$ deactivate`

#### NAVIGATE AND EXPLORE

* Print the working directory: `$ pwd`
* Go back to a directory: `$ cd ..`
* Go two directories back: `$ cd ../..`
* List the files in a specific directory: `$ ls <dir_name>`
* Go to Root directory: `$ cd /`
* Go to Home directory: `$ cd [ENTER]`
* View items in list view with details: `$ ls -l` (use -lt or add -t to sort)
* View files with a specific file extension: `$ ls *<.extn>`
* Current directory: `$ .`
* Open a file: `$ open <file_path>`
* Print the last executed statement: `$ _`
* View hidden files: `$ ls -a`

#### WORKING FILES AND DIRECTORIES

* Create a directory: `$ mkdir <dir_name>`
* Create multiple directories: `$ mkdir <dir1> <dir2> <dirN>`
* Create a file: `$ touch <file_name>`
* Read a file: `$ cat <file_name>`
* Write to a file: `$ echo "<text>" >> <file_name>` (use > to rewrite the text)
* Create a file in a directory using echo: `$ echo "<text>" > <file_name>`
* Print text of multiple files together: `$ cat <file1> <file2>`
* Concatenate content of multiple files: `$ cat <file1> <file2> > <file3>`
* Move file: `$ mv <file_name> <dir_path>`
* Rename file: `$ mv <file_name> <new_name>`
* Copy file: `$ cp <copy_file> <copied_file>`
* Remove file: `$ rm <fine_name>` (this will remove file not dir)
* Remove dir: `$ rm -rf <dir_name>` (r - recursive, f - force)

#### PYTHON

* Open Python terminal: `$ python`
* Execute a command: `$ python -c "print('Real Python')"`
* Exit Python terminal: `>>> exit()` (or \\[CRTL]D)

#### JUYPTER LAB

* Start JupyterLab: `$ jupyter lab`

#### RASA

* Create new project: `$ rasa init --no-prompt`
* Train model: `$ rasa train`
* Test assistant: `$ rasa train`
* Talk to assistant: `$ rasa shell`

#### PIP

* Pip install package: `$ pip install <package-name>`
* Pip uninstall package: `$ pip uninstall <package-name>`
* Pip help: `$ pip --help`
