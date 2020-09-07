# Overview
* [Intro](#version-control)
* [Installing Git](#installing-git)
* [Making a GitHub Account](#making-a-github-account)
* [Getting Started](#getting-started-with-git)
* [Basic git commands](#basic-git-commands)
* [Pull Requests](#pull-requests)
* [Best Practices](#best-practices)

# Version Control
Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later and keep track of your changes.

### Why use Git?
- Keep a history of your work
- Undo bad changes
- Work on the same project with others
- Backup your code to the Internet

### What can I store in Git?

*Short answer:* Anything!

*Longer answer:* Anything that is in a plain-text format (e.g. source code, text files, HTML) can be tracked by Git very well. Binary files also can be tracked, but you shouldn't put certain binary files into Git. **You shouldn't add generated executable files and object-code (.class, .pyc) because those files can be built using the source code.** Images are generally okay to add, and GitHub will even show the differences in images!

### Git and GitHub

What's the difference between Git and GitHub? Git is a distributed version-control system for tracking changes in source code repositories, while Github is a company that hosts Git repositories.

## Installing Git

We've listed some brief instructions below, but if you run into issues, follow the [instructions from the Git website](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install Git.

#### Linux
Install Git using your package manager (e.g. `sudo apt install git` in the case of Ubuntu).

#### Mac OSX
Open a terminal and type `git`. If you get a prompt to install Xcode command line tools, let it install.

If you're impatient or want the latest version, you can install Git with this [download](https://git-scm.com/download/mac) (you may need to follow [this guide](https://github.com/timcharper/git_osx_installer#i-have-xcode-installed-and-consequently-its-bundled-git-how-do-i-get-my-system-to-use-this-version-instead)).

#### Windows
You can download Git from [here](https://git-for-windows.github.io/).

## Making a GitHub Account

Go to [GitHub](https://github.com/) and sign up for an account -- it's free!

![terminal image](images/github_initial.png)

*Note:* If you're a student, you can apply for the pro version by following [these instructions](https://help.github.com/en/articles/applying-for-a-student-developer-pack).

## Getting Started with Git

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

## Basic Git Commands

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

## Pull Requests

Pull requests help users contribute to shared repositories. They're the main means by which people contribute to open source software.

If you're interested in learning more about how to make a pull request, check out [this section](making_a_pull_request.md).

## Best Practices

#### Frequent Commits
Commits should be made as **frequently** as possible. Frequent commits allow you to easily revert changes, and will leave you with a descriptive log of what changes you've made since you started working.

#### Descriptive Commit Messages
Commits should act as snapshots of your code. By adding descriptive commits, you'll make it easier to identify what your changes did.
