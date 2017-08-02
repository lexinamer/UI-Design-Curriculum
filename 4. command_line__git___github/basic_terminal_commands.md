---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE0NiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.faTbFFsI0zVgvvvs-ZXWqcots2UL4qK0WwzV_86T06s

title: >-
  Basic Terminal Commands
description: >-
  Basic Terminal Commands
---
# What is the command line? 
Sometimes referred to as the command screen or a text interface, the command line (or Terminal on Mac) is a user interface that is navigated by typing commands at prompts, instead of using the mouse. We will be using iTerm to navigate the command line. 

# Commands
*Note: for the following commands, you do not type the brackets, they indicate a placeholder. You do not type the $ either, that is to indicate you are on the command line.*

## Display the current working directory
```
$ pwd
```

## Changing the current working directory (must go in order of file tree on computer)
```
$ cd [<directory>]
```

### Examples:
- `cd ~` Change the current directory to the home directory (Essentially, "Go to the home directory")
- `cd ~/Desktop` Go to the Desktop
- `cd ..` Go _up_ a single directory


## Listing the contents of a given directory
```
$ ls [-a] [-l] [<directory>]
```

### Examples:
- `ls` List the files and subdirectories of the current directory
- `ls ~/Desktop` List the files and subdirectories of the desktop
- `ls -a` List **all** the files and subdirectories of the current directory. This includes even hidden "dotfiles".
- `ls -l` List the files and subdirectories in the current directory in the "long" format, which includes a lot more information.
- `ls -al ~/Desktop` The above three commands combined.


## Make a new directory
```
# make a directory
$ mkdir <directory_location>
```

### Examples:
- `mkdir ~/tiy` Make a new directory called `tiy` inside of the home directory.
- `mkdir tiy` Make a new directory called `tiy` inside your current location.
- `mkdir day-1` Make a new directory called `day-1` inside of the _current_ directory.

## Removing (or deleting) a file (CAUTION: this is irreversible!)
```
$ rm <filename>
```

### Examples:
- `rm hello.txt` Delete the file called `hello.txt` found in the _current_ directory.
- `rm ~/Desktop/embarrassing-photo.jpg` Delete the file `embarrassing-photo` from the desktop.


## Removing an entire directory (CAUTION: this is irreversible!)
```
$ rmdir <directory_name>
```
_(Be very careful with this command)_

### Examples:
- `rmdir my_old_dir` Delete the directory called `my_old_dir` found in the _current_ directory.
- `rmdir ~/Desktop/favorite_photos` Delete the directory called `favorite_photos` on the desktop. I don't think you want to do this.


## Open an file or directory from the terminal
```
# use Mac's default program to open a file or folder
$ open <filename-or-directory>
```

### Examples:
- `open my-file.txt` Open `my-file.txt` found in the _current_ directory with the default text editor.
- `open ~/Desktop/index.html` Open `index.html` on the desktop in the default web browser.
- `open ~/Pictures/0001.JPEG` Open `0001.JPEG` in Preview.


## Copy a file or directory
```
# copy: copy a file or directory to another directory
$ cp <filename> <directory-it-should-be-copied-to>
$ cp -R <directory> <directory-it-should-be-copied-to>
```

### Examples:
- `cp my-file.txt ~/Desktop` Copy `my-file.txt` from the _current_ directory and put the duplicate file on the desktop.
- `cp -R my_cool_files ~/Desktop` Copy the **entire** `my_cool_files` directory and put the duplicate directory on the desktop.

# Misc Commands

## Atom
```
$ atom . # open current working directory with Atom
$ atom <name_of_file> # Open a file in Atom (or create it and open if the file does not exist)
```

## Touch
```
# create a blank file if it doesn't exist, otherwise it updates the modified timestamp
$ touch <filename>
$ touch day01-notes.txt (makes empty text file in directory) 
```

## Common location shortcuts
- `.` The current directory
- `..` The parent directory of your current directory
- `~` Your home directory
- `-` Your previous directory (where you were before)
- `clear` clears screen 

## Common helpers
- `<up_arrow>` Cycle back through the last things you typed on the command line
- `<tab>` Text completion (start typing a command, hit tab, it finishes writing it)
- `!!` The last command, typically used like: `!!`

## More resources

- More shell config, tools, and apps: https://github.com/alebcay/awesome-shell
- More in-depth terminal walkthrough: https://github.com/jlevy/the-art-of-command-line

