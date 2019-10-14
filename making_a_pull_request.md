# Making a Pull Request

## What is a pull request?
A **pull request** (PR) tells others about changes that you want to make to a repository. They are great when you are working on a project with other people because they let everyone know about the changes you want to make. If you're working with a team on a shared repository, this lets each member view your changes and even comment and review your code.

Pull requests are typically used for **open source** projects that are managed through Git.

## Creating a pull request
One common flow for a pull request is as follows:

1. Fork the repository
2. Clone the forked repository
3. Create a new branch

### Forking
Forking the repository creates a copy of the current repository under your username. You can fork the repository by hitting the fork button on the upper right hand side of the page.
![forking repo](images/fork_repo.png)

### Cloning
Use the `clone` command to start editing a local copy of the repository.

Go the page with your newly forked repository and get the link to clone it. It should look something like this, but "your-username" is replaced with your github username.

`git clone https://github.com/your-username/IntroToProgrammingWorkshop.git`

### Creating a branch
A branch helps separate the changes you are making to a code base. The main branch of a project is typically called the **master** branch, and it's best practice to only use the master branch for final changes that you want to make live. When creating a branch try and create descriptive names, like `fix-workshop-typo` or `add-new-exercises` instead of `my-branch`.

To create a branch, start by entering the local copy of your repository

`cd IntroToProgrammingWorkshop`

Then use the branch command to create a new branch,

`git branch new-branch`

*Remember to swap out new-branch for a more descriptive name!*

Then to switch to that branch, use the checkout command

`git checkout new-branch`

**Tip**: If you want to combine the two previous steps into one command you can use `git checkout -b new-branch` (it creates *and* switches to the new branch)

If you ever want to switch back to the master branch, use `git checkout master`

Once you are on your newly created branch, you can add your changes with the typical git flow:

1. `git add file-name`
  * "file-name" is the name of the file you want to add
2. `git commit -m "message"`
 * "message" describes what the committed code does and is a little more descriptive
3. `git push --set-upstream origin new-branch`
 * "new-branch" is your branch name

## Getting started
To get started and make your first pull request, try following along [this repo](https://github.com/firstcontributions/first-contributions).

Once you get the hang of it, feel free to make pull requests for any of our repositories! Add an exercise, a personal project, or just fix a typo! Our organizers will try and review them as soon as possible.

## Sources
* [Creating a Pull Request](https://www.digitalocean.com/community/tutorials/how-to-create-a-pull-request-on-github)
