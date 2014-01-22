**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](2-version-control-intro.md)
[`main page`](http://github.com/engraving-challenges/main/)
[`next =>`](4-learning-git.md)

-------------------------------------------

HOW TO HANDLE GIT BEGINNNERS VS ADVANCED USERS?
I suggest the following: Make the instructions quite brief, and include links to git-reference.md (looking like "read more about pushing" "what's a commit?").  This reference would be intended to be used as a reference, i.e. not sequentially - you onlty read what parts interst you, and generally land there from links.

---

Set up necessary tools
----------------------

This document provides a concise description of our Git workflow.
It is not intended to introduce you to Git's concepts or tell you
how to achieve a specific task. If you're having problems to understand
or do this please contact us or visit our (work-in-progress)
[Git introduction](https://github.com/openlilylib/git-introduction).

### Read an introduction about Git

https://github.com/openlilylib/git-introduction/blob/master/old-git-basics.md


### Install [Git](http://git-scm.com/downloads)

-> [git-scm.com/downloads](http://git-scm.com/downloads)


### Create an account on [GitHub](http://github.com)

-> [github.com](http://github.com)


### Set up Git

Open the command line on your computer.  On Linux and MacOS, this will
probably be the "Terminal" app; on Windows, this will be the "Git Bash"
program installed with Git (_not the Windows command line_).

Tell Git your name and email, so that your work will be properly
attributed to you:

``` bash
git config --global user.name "Your Name Here"
git config --global user.email "your_email@example.com"
```

(This may or may not be the same as the data used for creating a GitHub account.)

### Haven't used command line before?

See [using-command-line.md]


Set up the challenge
--------------------

### Fork the challenge's repository

On the GitHub website, find the repository with the challenge that you
want to work on (they are listed [here](github.com/engraving-challenges))
and click `Fork` (in the upper-right corner).
This fork is *also* stored on GitHub, and you will have *write* access to it.


### Clone the repository to your computer

Open the command line again, [navigate](setup.md#havent-used-command-line-before)
to the directory where you want to place the repository and run
`git clone https://github.com/USER_NAME/REPO_NAME.git`,
replacing USER_NAME with your GitHub user name, and REPO_NAME
with the actual name of the challenge's repository.
(You may also copy the repository address from GitHub.  On the website
_of your fork_, find the `HTTPS clone URL` - it's located on the right).  


### Add upstream repository to your local clone

To be able to download any new work submitted by other participants,
you have to add a _remote repository_.  In the command line, navigate
to *inside your repository directory* and run
`git remote add upstream https://github.com/engraving-challenges/REPO_NAME.git`,
replacing REPO_NAME with the name of the challenge's repository.
This will add a remote with the name of `upstream` to the `origin` remote
that was initialized by `git clone` and that points to your fork on Github.



Submit your first commit
------------------------

A good way to check that everything is working correctly is to submit your first commit.  This is also a good way of announcing your participation in the challenge.

Open the command line, go to the repository and run `git status`.  It should report "On branch master [...] nothing to commit, working directory clean".

Create a subdirectory for yourself, with the name "notation-software-your-name" (for example `Finale-2014-John-Doe`).  Inside, create a `README.md` file (`.md` files are similar to `.txt` files).  In this file you may introduce yourself briefly.
Inside this directory you can do what you want, adding subdirectories
for any tools, include or intermediate files or whatever.

Run `git status` again - it should now list your directory under "Untracked files".  Use `git add your-directory-name` to tell git to start tracking it, and make a commit with `git commit -am 'brief description'`

Use `git push origin master` to "upload" your changes to your GitHub fork.  Now you want to share the changes from the fork to the original repository.  Go to your fork on GitHub click green `Compare & pull request` button.  You should be able to see your changes below.  If everything is in order, click `Send pull request`.

Committing, pushing and pull requests are described in more detail in later sections.


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](2-version-control-intro.md)
[`main page`](http://github.com/engraving-challenges/main/)
[`next =>`](4-learning-git.md)
