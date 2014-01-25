**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](2-version-control-intro.md)
[`main page`](README.md)
[`next =>`](4-learning-git.md)

-------------------------------------------

This section will tell you how to setup your copy of an engraving challenge repository.  It is not intended to introduce you to Git's concepts - for that, look at the [previous section](2-version-control-intro.md).


Set up necessary tools
----------------------

### Install Git

You can download Git [here](http://git-scm.com/downloads).


### Create an account on GitHub

Visit [github.com](http://github.com) website.


### Set up Git

Open the command line on your computer.  On Linux and MacOS, this will
probably be the "Terminal" app; on Windows, this will be the "Git Bash"
program installed with Git (_not the Windows command line_).

Tell Git your name and email, so that your work will be properly
attributed to you:

    git config --global user.name "Your Name Here"
    git config --global user.email "your_email@example.com"

(This may or may not be the same as the data used for creating a GitHub account.)

### Haven't used command line before?

Check out [these tips](using-command-line.md).



Set up the challenge
--------------------

### Fork the challenge's repository

Go to the GitHub page of the challenge's repository - they are listed [here](http://github.com/engraving-challenges) - and click `Fork` (in the upper-right corner).  This fork is *also* stored on GitHub, and you will have *write* access to it.


### Clone the repository to your computer

Open the command line, go to the directory into which you want to download the repository and run

    git clone https://github.com/USER_NAME/REPO_NAME.git

replacing USER_NAME with _your_ GitHub username, and REPO_NAME with challenge's repository name (e.g. `estrella`).


### Add upstream repository to your local clone

To be able to download new work submitted by other participants,
you have to add a _remote repository_.  In the command line, go
*inside your repository directory* and run

    git remote add upstream https://github.com/engraving-challenges/REPO_NAME.git

replacing REPO_NAME with the name of the challenge's repository.  This will add a remote named `upstream` that points to the challenge's official repository.



Submit your first commit
------------------------

This is a good way to check if everything is working correctly, and announce your participation in the challenge.

1. Create a subdirectory named "notationSoftware-yourName" (e.g. `Finale-2014-John-Doe`) in the repo.
2. Create an empty `README.md` file inside this subdirectory.
3. Tell Git to track this file with `git add *`.
4. Make a commit with `git commit -am 'New participant'`.
5. Upload your changes to your GitHub fork with `git push origin master`.
6. On your fork's GitHub webpage click `Compare & pull request` and then `Send pull request`.

If you're a bit confused, don't worry!  Next section will explain using Git in more detail, and at a more gradual pace.


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](2-version-control-intro.md)
[`main page`](README.md)
[`next =>`](4-learning-git.md)
