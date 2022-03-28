## The command LIne

- "As an example I will have typically 3 terminals open:
  - 1 in which I do my working,
  - 2 another to bring up ancillary data
  - 3 and a final one for viewing Manual pages"

### What is it? 

  - a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

  - The command line typically presents you with a prompt. As you type, it will be displayed after the prompt. Most of the time you will be issuing commands. 

### How does it work?

Within a terminal you have what is known as a shell. This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. There are various shells available but the most common one is called bash which stands for Bourne again shell. 


### What do I do to get to one?

- If you're on a Mac then you'll find the program Terminal under Applications -> Utilities. An easy way to get to it is the key combination 'command + space' which will bring up Spotlight, then start typing Terminal and it will soon show up.

- If on Linux then you will probably find it in Applications -> System or Applications -> Utilities. Alternatively you may be able to 'right-click' on the desktop and there may be an option 'Open in terminal'.

- If you are on Windows and intend to remotely log into another machine then you will need an SSH client. A rather good one is Putty (free) .

## Basic Navigation

pwd
- Print Working Directory - ie. Where are we currently.
ls
- List the contents of a directory.
cd
- Change Directories - ie. move to another directory.
Relative path
- A file or directory location relative to where we currently are in the file system.
Absolute path
- A file or directory location in relation to the root of the file system.

## More About Files

use `file path` to determine what type of file is listed when you use ls.

`file`
- obtain information about what type of file a file or directory is.

`ls -a`
- List the contents of a directory, including hidden files.

Everything is a file under Linux
- Even directories.

Linux is an extensionless system
- Files can have any extension they like or none at all.

Linux is case sensitive
- Beware of silly typos.

## Manual Pages

`man <command to look up>` - find definition of a terminal command

`man -k <search term>` - to search the manual pages for a search term

-can learn about the flags associated with a command

### summary

man <command>
  -Look up the manual page for a particular command.
man -k <search term>
  -Do a keyword search for all manual pages containing the given search term.
/<term>
  -Within a manual page, perform a search for 'term'
n
  -After performing a search within a manual page, select the next found item.

The man pages are your friend.
  -Instead of trying to remember everything, instead remember you can easily look stuff up in the man pages.

## File Manipulation

mkdir
- Make Directory - ie. Create a directory.
rmdir
- Remove Directory - ie. Delete a directory.
touch
- Create a blank file.
cp
- Copy - ie. Copy a file or directory.
mv
- Move - ie. Move a file or directory (can also be used to rename).
rm
- Remove - ie. Delete a file.
No undo
- The Linux command line does not have an undo feature. Perform destructive actions carefully.
Command line options
- Most commands have many useful command line options. Make sure you skim the man page for new commands so you are familiar with what they can do and what is available.

## Cheat Sheet

- [a link to list all basic commands from Ryans tutorial in linux command lines](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

------------

## Observations and learnings

I learned I know most of the commands already, but it was a great refresher to practice some of the lesser used commands I use daily.

I will make sure I have this cheat sheet handy from Ryans Tutorial:
  - https://ryanstutorials.net/linuxtutorial/cheatsheet.php
