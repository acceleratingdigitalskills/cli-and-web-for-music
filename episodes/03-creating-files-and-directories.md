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
