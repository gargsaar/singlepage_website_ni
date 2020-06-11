---
date: 2020-06-04T08:18:58.000Z
layout: post
title: 10 Features Every Python Programmer Must Know
subtitle: A curated list of very powerful Python features
description: A curated list of not so common, but very powerful Python features
  that every Python programmer must know
image: /assets/images/post_images/command-line.jpeg
optimized_image: /assets/images/post_images/command-line.jpeg
category: Python
tags:
  - Python
author: sarthakgarg
paginate: true
---
Interacting with a computer through a command-line interface (CLI) is a powerful technique. Mastering the command line can greatly improve your productivity during development. Below is a list of the most fundamental commands for navigating, manipulating and inspecting files.

PYTHON\
`Open Python terminal: $ python`\
`Exit Python terminal: >>> exit() (or [CRTL]D)`\
`Print the last executed statement: $ _`\
`Execute a command: $ python -c "print('Real Python')"`

MAC OS\
`Map Python Version: $ echo "alias python=/usr/local/bin/python3.7" >> ~/.zshrc`\
`Exit i.e. terminate any current process and start new line: $ ^c (^ = [CTRL])`\
`Find out the language of the terminal (zsh/bash/sh) : $ echo $0`\
`Read manual of command: $ man <cmd> ([ENTER] to scroll, q to quit)`\
\
VIRTUAL ENV\
`Create a new virtual environment: $ python -m venv <dir_name>`\
`Goto <dir_name>/bin, activate: $ source activate (This will prepend the path to “venv” at the beginning of the $PATH variable. )`\
`Exit the virtual environment: $ deactivate`

JUYPTER LAB\
`Start JupyterLab: $ jupyter lab`

NAVIGATE AND EXPLORE\
`Print working directory: $ pwd`\
`Go back to a directory: $ cd ..`\
`Go two directories back: $ cd ../..`\
`List the files in a specific directory: $ ls <dir_name>`\
`Go to Root directory: $ cd /`\
`Go to Home directory: $ cd [ENTER]`\
`View items in list view with details: $ ls -l (use -lt or add -t to sort)`\
`View files with a specific file extension: $ ls *<.extn>`\
`Current directory: $ .`\
`Open a file: $ open <file_path>`\
`View hidden files: $ ls -a`

CREATE FILES AND DIRECTORIES, WORKING WITH FILES\
`Create a directory: $ mkdir <dir_name>`\
`Create multiple directories: $ mkdir <dir1> <dir2> <dirN>`\
`Create a file: $ touch <file_name>`\
`Read a file: $ cat <file_name>`\
`Write to a file: $ echo "<text>" >> <file_name> (use > to rewrite the text)`\
`Create a file in a directory using echo: $ echo "<text>" > <file_name>`\
`Print text of multiple files together: $ cat <file1> <file2>`\
`Concatenate content of multiple files in a file: $ cat <file1> <file2> > <file3>`\
`Move file: $ mv <file_name> <dir_path>`\
`Rename file: $ mv <file_name> <new_name>`\
`Copy file: $ cp <copy_file> <copied_file>`\
`Remove file: $ rm <fine_name> (this will remove file not dir)`\
`Remove dir: $ rm -rf <dir_name> (r - recursive, f - force)`