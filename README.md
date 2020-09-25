# GIT-Doc

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

But, what's *Local repository*? <br>
Easy. When we type `git init`, git creates a hidden folder inside our working directory. We mustn't edit this repository. The files that get uploaded in it, will be the ones that we are going to send to Git to make a copy of it in the cloud.

When the files are in the working directory, Git doesn't "listen" to them, but it will know if they are being edited, so we must send them to the staging area, using `git add [file name / . (every file)]`.

In the staging area, we can check which are the changes that will be made to the Git files when we upload them. To send them to our *local repository* we need to type `git commit -m "[message]"`. Make sure to set a message in each commit, this wil be useful in the future.

Finally, to get our files uploaded or updated in our Git repository, use `git push`.

## Commits

Basically, a **commit** is a photo of our files and the hierarchy of our project. Every commit will be saved in our local repository. If we need to check them, we can type `git log --oneline`, this will show us a summary of each one of them. Each commit will have a code before it's message.

*I've messed my project, I need backup!*<br>
