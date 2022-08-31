# command line

A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands.

example:

```
user@bash: ls -l /home/ryan
total 3
drwxr-xr-x  2 ryan users 4096 Mar 23 13:34 bin
drwxr-xr-x 18 ryan users 4096 Feb 17 09:12 Documents
drwxr-xr-x  2 ryan users 4096 May 05 17:25 public_html
user@bash:
```

### The Shell, Bash

Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell. This tutorial will assume you are using bash as your shell.

If you would like to know which shell you are using you may use a command called echo to display a system variable stating your current shell. echo is a command which is used to display messages.

```
user@bash: echo $SHELL
/bin/bash
user@bash:
```

### Shortcuts

The terminal may seem daunting but don't fret. Linux is full of shortcuts to help make your life easier. You'll be introduced to several of them throughout this tutorial. Take note of them as not only do they make your life easier, they often also save you from making silly mistakes such as typos.

##### So where are we?

```
user@bash: pwd
/home/aziz
user@bash:
```

##### What's in Our Current Location?

```
user@bash: ls
bin Documents public_html
user@bash:
```

## Paths

In the previous commands we started touching on something called a path. I would like to go into more detail on them now as they are important in being proficient with Linux. Whenever we refer to either a file or directory on the command line, we are in fact referring to a path. ie. A path is a means to get to a particular file or directory on the system.

## Let's Move Around a Bit

```
user@bash: pwd
/home/ryan
user@bash: cd Documents
user@bash: ls
file1.txt file2.txt file3.txt
...
user@bash: cd /
user@bash: pwd
/
user@bash: ls
bin boot dev etc home lib var
...
user@bash: cd ~/Documents
user@bash: pwd
/home/ryan/Documents
user@bash: cd ../../
user@bash: pwd
/home
user@bash: cd
user@bash: pwd
/home/ryan
```

## More About Files!

##### Everything is a File

Ok, the first thing we need to appreciate with linux is that under the hood, everything is actually a file. A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. To begin with, this won't affect what we do too much but keep it in mind as it helps with understanding the behaviour of Linux as we manage files and directories.

#### Linux is an Extensionless System

This one can sometimes be hard to get your head around but as you work through the sections it will start to make more sense. A file extension is normally a set of 2 - 4 characters after a full stop at the end of a file, which denotes what type of file it is. The following are common extensions:

#### Linux is Case Sensitive

## Manual Pages!

The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept.

You invoke the manual pages with the following command:

```
user@bash: man ls
Name
    ls - list directory contents

Synopsis
    ls [option] ... [file] ...

Description
    List information about the FILEs (the current directory by default). Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

    Mandatory arguments to long options are mandatory for short options too.

    -a, --all
        do not ignore entries starting with .

    -A, --almost-all
        do not list implied . and ..

...
```

#### Searching

It is possible to do a keyword search on the Manual pages.

# File Manipulation!

To begin with we'll learn to make some files and directories and move them around.

### Making a Directory

Linux organises it's file system in a hierarchical way. Over time you'll tend to build up a fair amount of data (storage capacities are always increasing).

```
user@bash: mkdir linuxtutorialwork
```

The first one is -p which tells mkdir to make parent directories as needed (demonstration of what that actually means below). The second one is -v which makes mkdir tell us what it is doing.

#### Removing a Directory

```
user@bash: rmdir linuxtutorialwork/foo/bar
```

#### Creating a Blank File

```
user@bash: touch example1
```

#### Copying a File or Directory

```
user@bash: ls
example1 foo
user@bash: cp example1 barney
user@bash:ls
barney example1 foo
```

#### Moving a File or Directory

To move a file we use the command mv which is short for move. It operates in a similar way to cp. One slight advantage is that we can move directories without having to provide the -r option.

```
user@bash: ls
barney example1 foo foo2
user@bash: mkdir backups
user@bash: mv foo2 backups/foo3
user@bash: mv barney backups/
user@bash: ls
backups example1 foo
```

#### Renaming Files and Directories

```
user@bash: ls
backups example1 foo
user@bash: mv foo foo3
user@bash: ls
backups example1 foo3
user@bash: cd ..
user@bash: mkdir linuxtutorialwork/testdir
user@bash: mv linuxtutorialwork/testdir /home/ryan/linuxtutorialwork/fred
user@bash: ls linuxtutorialwork
backups example1 foo3 fred
```

#### Removing a File

```
user@bash: ls
backups example1 foo3 fred
user@bash: rm example1
user@bash: ls
backups foo3 fred
```

#### Removing non empty Directories

```
user@bash: ls
backups foo3 fred
user@bash:  rmdir backups
rmdir: failed to remove 'backups': Directory not empty
user@bash: rm backups
rm: cannot remove 'backups': Is a directory
user@bash: rm -r backups
user@bash: ls
foo3 fred
```

[cheat sheet](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
