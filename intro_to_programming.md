# Intro to Programming

- [What is the terminal?](#what-is-the-terminal)
  * [Why use the terminal?](#why-use-the-terminal)
  * [How to open the terminal](#how-to-open-the-terminal)
  * [File Structure](#file-structure)
  * [Terminal Navigation](#terminal-navigation)
  * [Basic Commands](#basic-commands)
  * [Cheatsheet](#cheatsheet)
  * [Input and Output processing](#input-and-output-processing)
- [Version Control](#version-control)
  * [Why use Git?](#why-use-git)
  * [Git and Github](#git-and-github)
  * [Getting Started](#getting-started-with-git)
  * [Basic git commands](#basic-git-commands)
  * [Pull Requests](#pull-requests)
  * [Best Practices](#best-practices)

## What is the terminal?

The terminal is a command line interface which takes commands from a user, lets the computer process the commands, and displays the output.

### Why use the terminal?
While graphical user interfaces (GUIs) are helpful for a lot of things, sometimes command line interfaces (CLIs) are the better tool for the job.

As an example, imagine you have a messy folder, and you want to combine all the .txt files into a new file called `newfile.txt`. If you use a GUI, this seems like a tedious task, but it only takes one line in the terminal.

```
cat *.txt > newfile.txt
```

### How to open the terminal

#### Mac OS
Follow these steps to open the terminal:

1. Open *Finder* from the Dock.
2. Open your *Applications* folder.
3. Open *Utilities*.
4. Double click on *Terminal*.

![terminal image](images/terminal.png)

#### Ubuntu
Hit the keyboard shortcut Ctrl - Alt - T, or search for it via the menu at the bottom of the dock.

#### Windows
Windows also has a built-in terminal, Command Line (or `cmd`); however, Command Line differs greatly from the shells on Mac and Linux, so we will not cover the specifics of how to work with it.

The Windows installation of Git comes with a version of Bash (the shell found on Mac and Linux). **This tutorial follows Bash conventions, so we recommend installing Git for Windows users**. You can get Git (and its version of Bash) [here](https://git-for-windows.github.io/).

*Note:* If you'd prefer, Windows comes with Powershell, which supports many common Linux commands.

### File Structure
#### Directories
Computers organize files with directories. A directory contains a group of files. If you want, you can create subdirectories within a directory to organize further.

*Note:* Each file within a given directory must have a unique name, but files contained in different directories do not.

#### Home Directory and Pathnames
Unix associates each user with a directory. When you open your terminal, you are placed in your home directory.

![directory image](images/file_tree.jpg)

The **root** directory is at the top of the file tree (a couple layers above all of the home directories).

When you are inside a directory, it is called your **current working directory**.

You can change directories by specifying the appropriate pathname. There are two ways to specify a pathname.

**1. Absolute Pathname**: Describes how to reach a file from the root directory.

```
/Users/username/hackbu/IntroToProgrammingWorkshop
```
*Note:* Absolute pathnames always begin with a `/` (slash).

**2. Relative Pathname**: Describes how to reach a file from the current directory.

```
./sample_directory/sample.txt
```
*Note:* Relative pathnames will never begin with a  `/` (slash), and by convention, `..` always refers to the parent directory (one level higher than your current directory) and `.` refers to your current directory.

### Terminal Navigation
Here's a list of helpful commands for moving around your computer's filesystem.

* `pwd` tells you what directory you are in
* `cd destination_directory` moves you from your current directory into the directory you specify
* `ls` lists the files in your current directory
* `mv source_file destination_file` renames `source_file` as `destination_file`

### Basic Commands

* `man command_name` opens a manual page for the command you provide -- to exit the manual, press `q`
* `echo "hello"` prints out `hello` to the command line
* `touch filename` creates an empty file with the specified name
* `cat filename` prints the contents of the specified file
* `cp source_file destination_file` creates a copy of `source_file` named `destination_file`
  - *Note:* It will overwrite the destination file if one of the same name already exists
* `rm file` removes the specified file
  - *Note:* You can remove more than one file at a time by specifying multiple files, e.g. `rm file_1 file_2 file_3`
* `mkdir directory_name` creates a directory with the specified name
* `rmdir directory_name` removes the specified directory (only if it's empty)
  * *Note:* If you want to remove a directory and its contents, you can use `rm -rf directory_name`
### Cheatsheet
| Command        | What it means            |
| ------------- |:-------------:|
| man     | get the manual pages of a command if available |
| pwd     | print working directory |
| ls      | list files      |
| cd | change directory      |
| cat | display file contents      |
| cp | make a copy of a file  |
| mkdir | make a directory  |
| mv | rename or move a file  |
| rm | remove a file |

### Input and Output Processing

#### Output Redirection

You can use `>` to redirect output from the terminal interface to another file, for example:
```
$ echo hello
hello
$ echo hello > file
$ cat file
hello
```
*Note:* This will overwrite any existing data. To append text instead of overwriting it, you can use `>>`:

```
$ echo hello again >> file
$ cat file
hello
hello again
```
*Note:* If you want to append or write the contents of one file to another, you can redirect the output of the `cat` command.

#### Input Redirection

You can use `<` to redirect input from a file. Only use this when a program takes user input during execution (as opposed to from arguments like we've been using).

*Note:* Some commands should be used with input redirection. For example, the `wc -l` command returns the number of lines from a given file:

```
$ wc -l < file.txt
8
```

## Version Control
Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later and keep track of your changes.

### Why use Git?
- Keep a history of your work
- Undo bad changes
- Work on the same project with others
- Backup your code to the Internet

### Git and GitHub

What's the difference between Git and GitHub? Git is a distributed version-control system for tracking changes in source code repositories, while Github is a company that hosts Git repositories.

#### What can I store in Git?
*Short answer:* Anything!

*Longer answer:* Anything that is in a plain-text format (e.g. source code, text files, HTML) can be tracked by Git very well. Binary files also can be tracked, but you shouldn't put certain binary files into Git. **You shouldn't add generated executable files and object-code (.class, .pyc) because those files can be built using the source code.** Images are generally okay to add, and GitHub will even show the differences in images!

### Installing Git

We've listed some brief instructions below, but if you run into issues, follow the [instructions from the Git website](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install Git.

##### Linux
Install Git using your package manager (e.g. `sudo apt install git` in the case of Ubuntu).

##### Mac OSX
Open a terminal and type `git`. If you get a prompt to install Xcode command line tools, let it install.

If you're impatient or want the latest version, you can install Git with this [download](https://git-scm.com/download/mac) (you may need to follow [this guide](https://github.com/timcharper/git_osx_installer#i-have-xcode-installed-and-consequently-its-bundled-git-how-do-i-get-my-system-to-use-this-version-instead)).

##### Windows
You can download Git from [here](https://git-for-windows.github.io/).

### Making a GitHub account

Go to [GitHub](https://github.com/) and sign up for an account -- it's free!

![terminal image](images/github_initial.png)

*Note:* If you're a student, you can apply for the pro version by following [these instructions](https://help.github.com/en/articles/applying-for-a-student-developer-pack).

### Getting Started with Git

#### Configure Git

Git needs to know what your name and email is in order to label your changes on repositories. Use the below commands to set these values.

*Note:* You don't need to use your real name or email for this, if you're concerned about privacy.

```
# Setting user name and email
git config --global user.name "Test User"'
git config --global user.email "testuser@gmail.com"'
```

#### Make a Project

1. In your terminal, type `mkdir myproject` and `cd myproject` to create and enter a project directory.
2. To make your current directory a Git repository, just type `git init`.
3. Now that you have a directory with Git enabled, you can use the directory just like any other directory.
4. Write or copy some files into the directory, and then type `git status`. This will show you the current status of what's available to add to Git.
5. Under *Untracked Files*, you'll see the files that are in the directory, but not stored in Git.

#### Save Changes

1. To start tracking a file, type `git add myfile.txt`.
2. This hasn't saved the changes yet -- we need to ask Git to do that.
3. When you're ready to save your changes, type `git status` to review what's going to be saved.
4. If it all looks good, type `git commit -m "Describe what you've changed in these quotes"`.
5. To see what was saved, type `git show`. If you want to see a log of all of your previous commits, type `git log`.

### Basic Git Commands
| Command        | What it means            |
| ------------- |:-------------:|
| `git init`   | Initializes an empty git repository|
| `git add .`     | Adds all files in and below the current directory |
| `git add <file1>`     | Add a specific file |
| `git add <folder>`     | Add a folder |
| `git remove <file>`     | Remove a specific file |
| `git commit <file> -m  "message"`      | Commits with a message      |
| `git log`      | Display git commit history   |
| `git status`      | Show files added to the index, files with changes, and untracked files |
| `git pull`      | Fetches from remote to merge with the current branch |
| `git push`      | Uploads local content to a remote repository |
| `git clone <url> `      | Clone a repository from a URL    |

#### Common git flow

```
git init # only needed once
git add <file>
git commit -m "commit message"
git remote add origin <repo_name> # only needed once
git push -u origin master
```

### Pull Requests
Pull requests help users contribute to shared repositories. They're the main means by which people contribute to open source software.

If you're interested in learning more about how to make a pull request, check out [this section](making_a_pull_request.md).

### Best Practices
#### Frequent Commits
Commits should be made as **frequently** as possible. Frequent commits allow you to easily revert changes, and will leave you with a descriptive log of what changes you've made since you started working.

#### Descriptive Commit Messages
Commits should act as snapshots of your code. By adding descriptive commits, you'll make it easier to identify what your changes did.
