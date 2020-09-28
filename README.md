# GIT Documentation

**Guide**
* [First of all (GitHub Structure)](https://github.com/galindroid/GIT-Doc#first-of-all-github-structure)
* [Commit](https://github.com/galindroid/GIT-Doc#commits)
* [Branches](https://github.com/galindroid/GIT-Doc#branches)
* [Tags](https://github.com/galindroid/GIT-Doc#tags)

![Scheme of Github Structure](https://bluuweb.github.io/tutorial-github/img/git-flujo.png)

There are two ways of creating a __repository__ using Git.

* Using `git clone [URL repository]` (This will create a *new* folder, using the nae of the Github repository.)
* Using `git init`

Once we have linked our repository, we can make sure that everything went OK by using `git status`, this command line will give us information about all of our files.

We can use `git status -s` to check __ONLY__ those which have changed.

## First of all (GitHub Structure)

We need to know how does Git work.

We have 2 repositories:

* Local
* Github

They are linked, Git will know if any files are different between both of them. Using commands we can copy our files to the Github repository and vice versa.

In our local repository, our files must be in 3 different stages before getting *pushed* (copied to the Git repository). Those stages are:

* Working directory
* Staging area
* Local repository

***What's a Local repository?*** <br>
Easy. When we type `git init`, git creates a hidden folder inside our working directory. We mustn't edit this repository. The files that get uploaded in it, will be the ones that we are going to send to Git to make a copy of it in the cloud.

When the files are in the working directory, Git doesn't "listen" to them, but it will know if they are being edited, so we must send them to the staging area, using `git add [file name / . (every file)]`

In the staging area, we can check which are the changes that will be made to the Git files when we upload them. To send them to our *local repository* we need to type `git commit -m "[message]"` Make sure to set a message in each commit, this wil be useful in the future.

Finally, to get our files uploaded or updated in our Git repository, use `git push`

## Commits

Basically, a **commit** is a photo of our files and the hierarchy of our project. Every commit will be saved in our local repository. If we need to check them, we can type `git log --oneline`, this will show us a summary of each one of them. Each commit will have a code before it's message.

***I've fucked up my project, I need backup!***<br>
Use `git reset --hard [commit code]` To get the code, use `git log --oneline`

## Branches

When we create a repository, we create a main branch called *master*. The whole project is meant to be changed here, but we can create secondry branches if we need to do so, this is useful when we want to develop new charateristics to our project knowing that we won't affect to our colleagues's codes.

To create a new branch, type `git branch [new branch name]`

When we have a complex project, we'll probably have multiple branches. Use `git branch` to get info about which branch you're using. 

In this cases, we are, obviously, able to move between branches. <br> In order to do so, type `git checkout [destiny branch name]`

When we are finished making changes and we want to add them to our master branch, we must access to the master branch and type `git merge [branchName]` using the name of the branch we want to add. This will delete it after saving its changes to the master branch.

If we don't want a previously created branch, we can delete it by typing `git branch -d [branchName]`

***Tip***<br>
We can also create *AND* travel to that new branch using `git checkout -b [new branchName]`

## Tags

Tags create new versions to get, in the future, released. Also, we can set a text to each tag, so we can be able to recognize them.

* `git tag versionAlpha -m [tagName]` to create a new tag.
* `git tag` lists every tag we have created.
* `git tag -d [tagName]` deletes the specified tag.
* `git tag -a [tagName] [commitCode] -m [tagMessage]` creates a tag from an existing commit and adds a message to it.