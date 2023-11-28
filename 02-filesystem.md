---
title: "Navigating the Filesystem"
teaching: 0
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions

- How can I move around on my computer?
- How can I see what files and directories I have?
- How can I specify the location of a file or directory on my computer?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Understand the filesystem tree and explain how to navigate between directories
- Explain the function of the commands `ls`, `pwd` and `cd`
- Demonstrate how to view and move around inside a file hierarchy

- Explain the similarities and differences between a file and a directory.
- Translate an absolute path into a relative path and vice versa.
- Construct absolute and relative paths that identify specific files and directories.
- Use options and arguments to change the behaviour of a shell command.
- Demonstrate the use of tab completion and explain its advantages.

::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: instructor

Introducing and navigating the filesystem in the shell
(covered in [Navigating Files and Directories](02-filedir.md) section)
can be confusing. You may have both terminal and GUI file explorer
open side by side so learners can see the content and file
structure while they're using terminal to navigate the system.

::::::::::::::::::::::::::::::::::::::::::::::::::

The part of the operating system responsible for managing files and directories
is called the **file system**.
It organizes our data into files,
which hold information,
and directories (also called 'folders'),
which hold files or other directories.

Several commands are frequently used to create, inspect, rename, and delete files and directories.
To start exploring them, we'll go to our open shell window.

First, let's find out where we are by running a command called `pwd`
(which stands for 'print working directory'). Directories are like *places* — at any time
while we are using the shell, we are in exactly one place called
our **current working directory**. Commands mostly read and write files in the
current working directory, i.e. 'here', so knowing where you are before running
a command is important. `pwd` shows you where you are:

```bash
$ pwd
```

```output
/Users/nelle
```

Here,
the computer's response is `/Users/nelle`,
which is Nelle's **home directory**:

:::::::::::::::::::::::::::::::::::::::::  callout

## Home Directory Variation

The home directory path will look different on different operating systems.
On Mac, it is `/Users/nelle`, on Linux, `/home/nelle`,
and on Windows, it will be similar to `C:\Documents and Settings\nelle` or
`C:\Users\nelle`.
(Note that it may look slightly different for different versions of Windows.)
In future examples, we've used Mac output as the default - Linux and Windows
output may differ slightly but should be generally similar.

We will also assume that your `pwd` command returns your user's home directory.
If `pwd` returns something different, you may need to navigate there using `cd`
or some commands in this lesson will not work as written.
See [Exploring Other Directories](#exploring-other-directories) for more details
on the `cd` command.


::::::::::::::::::::::::::::::::::::::::::::::::::

To understand what a 'home directory' is,
let's have a look at how the file system as a whole is organized.  For the
sake of this example, we'll be
illustrating the filesystem on our scientist Nelle's computer.  After this
illustration, you'll be learning commands to explore your own filesystem,
which will be constructed in a similar way, but not be exactly identical.

On Nelle's computer, the filesystem looks like this:

![](fig/filesystem.svg){alt='The file system is made up of a root directory that contains sub-directoriestitled bin, data, users, and tmp'}

The filesystem looks like an upside down tree. 
The topmost directory  is the **root directory**
that holds everything else.
We refer to it using a slash character, `/`, on its own;
this character is the leading slash in `/Users/nelle`.

Inside that directory are several other directories:
`bin` (which is where some built-in programs are stored),
`data` (for miscellaneous data files),
`Users` (where users' personal directories are located),
`tmp` (for temporary files that don't need to be stored long-term),
and so on.

We know that our current working directory `/Users/nelle` is stored inside `/Users`
because `/Users` is the first part of its name.
Similarly,
we know that `/Users` is stored inside the root directory `/`
because its name begins with `/`.

:::::::::::::::::::::::::::::::::::::::::  callout

## Slashes

Notice that there are two meanings for the `/` character.
When it appears at the front of a file or directory name,
it refers to the root directory. When it appears *inside* a path,
it's just a separator.


::::::::::::::::::::::::::::::::::::::::::::::::::

Underneath `/Users`,
we find one directory for each user with an account on Nelle's machine,
her colleagues *imhotep* and *larry*.

![](fig/home-directories.svg){alt='Like other directories, home directories are sub-directories underneath"/Users" like "/Users/imhotep", "/Users/larry" or"/Users/nelle"'}

The user *imhotep*'s files are stored in `/Users/imhotep`,
user *larry*'s in `/Users/larry`,
and Nelle's in `/Users/nelle`. Nelle is the user in our
examples here; therefore, we get `/Users/nelle` as our home directory.
Typically, when you open a new command prompt, you will be in
your home directory to start.

Now let's learn the command that will let us see the contents of our
own filesystem.  We can see what's in our home directory by running `ls`:

```bash
$ ls
```

```output
Applications Documents    Library      Music        Public
Desktop      Downloads    Movies       Pictures
```

(Again, your results may be slightly different depending on your operating
system and how you have customized your filesystem.)

`ls` prints the names of the files and directories in the current directory.
We can make its output more comprehensible by using the `-F` **option**
which tells `ls` to classify the output
by adding a marker to file and directory names to indicate what they are:

- a trailing `/` indicates that this is a directory
- `@` indicates a link
- `*` indicates an executable

Depending on your shell's default settings,
the shell might also use colors to indicate whether each entry is a file or
directory.

```bash
$ ls -F
```

```output
Applications/ Documents/    Library/      Music/        Public/
Desktop/      Downloads/    Movies/       Pictures/
```

Here,
we can see that the home directory contains only **sub-directories**.
Any names in the output that don't have a classification symbol
are **files** in the current working directory.

:::::::::::::::::::::::::::::::::::::::::  callout

## Clearing your terminal

If your screen gets too cluttered, you can clear your terminal using the
`clear` command. You can still access previous commands using <kbd>↑</kbd>
and <kbd>↓</kbd> to move line-by-line, or by scrolling in your terminal.


::::::::::::::::::::::::::::::::::::::::::::::::::
