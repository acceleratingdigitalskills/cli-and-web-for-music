---
title: "Creating files and directories"
teaching: 0
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions

- How do I create, delete, copy, and move files and directories on my computer?
- How can I identify the location of files on my computer?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Create a directory hierarchy that matches a given diagram 
- Create empty files in the filesystem at a given location
- Delete specified files and/or directories
- Copy and move files and/or folders from and to a specified location
 
::::::::::::::::::::::::::::::::::::::::::::::::



::::::::::::::::::::::::::::::::::::: challenge 

## Working with files and folders

As well as navigating directories, we can interact with files on the command line: we can read them, open them, run them, and even edit them. In fact, there's really no limit to what we *can* do in the shell, but even experienced shell users still switch to graphical user interfaces (GUIs) for many tasks, such as editing formatted text documents (Word or OpenOffice), browsing the web, converting sound files from one format to another, etc. But if we wanted to do this hundreds of music tracks, say then we could automate that conversion work by using shell commands.

Before getting started, we will use `ls` to list the contents of our current directory. Using `ls` periodically to view your options is useful to orient oneself.

```bash
$ ls
```

### Copy and moving files into subdirectories

Start with the following filesystem hierarchy:

```
/Users/jamie/data
    - chords.json
```

Assume your username is `jamie`. Reorder the following commands

- `cp recombined/chords.json ../chords-backup.json`
- `cd ~/data`
- `mv chords.json recombined/`
- `mkdir recombined`

so that when you execute the following commands, they return the output as shown:

```bash
$ ls
recombined

$ ls recombined
chords.json
```
:::::::::::::::::::::::: solution 

- `cd ~/data`
- `cp recombined/chords.json ../chords-backup.json`
- `mkdir recombined`
- `mv chords.json recombined/`

:::::::::::::::::::::::::::::::::


### Try another way

Can you think of another way to achieve the same effect?

:::::::::::::::::::::::: solution 

There are lots.
  
:::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::  challenge

## Using `history`

Use the `history` command to see a list of all the commands you've entered during the current session. You can also use <kbd>Ctrl</kbd> + <kbd>r</kbd> to do a reverse lookup. Press <kbd>Ctrl</kbd> + <kbd>r</kbd>, then start typing any part of the command you're looking for. The past command will autocomplete. Press `enter` to run the command again, or press the arrow keys to start editing the command. If multiple past commands contain the text you input, you can <kbd>Ctrl</kbd> + <kbd>r</kbd> repeatedly to cycle through them. If you can't find what you're looking for in the reverse lookup, use <kbd>Ctrl</kbd> + <kbd>c</kbd> to return to the prompt. If you want to save your history, maybe to extract some commands from which to build a script later on, you can do that with `history > history.txt`. This will output all history to a text file called `history.txt` that you can later edit. To recall a command from history, enter `history`. Note the command number, e.g. 2045. Recall the command by entering `!2045`. This will execute the command.

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::: keypoints
 - `cp` copies data from one location (a source) to another (a target)
 - `cp` takes its source(s) and target as arguments
 - `mkdir` can be used to create directories
 - `mv` can be used to move data from one location to another, and is similar to copying followed by deletion 
 - `cp` and `mv` modify your files, and can lead to data loss
::::::
