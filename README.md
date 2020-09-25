# GIT-Doc

![Scheme of Github Structure](https://bluuweb.github.io/tutorial-github/img/git-flujo.png)

There are two ways of creating a __repository__ using Git.

* Using `git clone [URL repository]` (This will create a *new* folder, using the nae of the Github repository.)
* Using `git init`

## First of all

We need to lnow how does Git work.

We have 2 repositories:

* Local
* Github

Once we have linked our repository, we can make sure that everything went OK by using `git status`, this command line will give us information about all of our files.

We can use `git status -s` to check __ONLY__ those which have changed. This will be very useful in the future to make sure what are we going to add to our staging area.