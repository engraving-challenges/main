**_Scores of Beauty_ Engraving Challenges**
[`<= Git introduction`](3-git-introduction.md)
[`Main page`](README.md)

-------------------------------------------

This document contains detailed step-by-step instructions on setting up
and using Git to work on the Engraving Challenges.  It assumes that you
are familiar with the [basics of version control](3-git-introduction.md).


#### Table of Contents:

* [Set up necessary tools](4-using-git.md#set-up-necessary-tools)
  - [Install Git](4-using-git.md#install-git)
  - [Set up Git](4-using-git.md#set-up-git)
  - [Create an account on GitHub](4-using-git.md#create-an-account-on-github)
* [Set up the challenge](4-using-git.md#set-up-the-challenge)
  - [Fork the challenge's repository](4-using-git.md#fork-the-challenges-repository)
  - [Clone the repository to your computer](4-using-git.md#clone-the-repository-to-your-computer)
  - [Add upstream repository to your local clone](4-using-git.md#add-upstream-repository-to-your-local-clone)
  - [Submit your first commit](4-using-git.md#submit-your-first-commit)
* [Git crash course](4-using-git.md#git-crash-course)
  - [git status is your friend](4-using-git.md#git-status-is-your-friend)
  - [Committing changes to the files](4-using-git.md#committing-changes-to-the-files)
  - [Adding new files to the repository](4-using-git.md#adding-new-files-to-the-repository)
  - [Important note about pdf files](4-using-git.md#important-note-about-pdf-files)
  - [Viewing your commits](4-using-git.md#viewing-your-commits)
  - [Pushing your changes](4-using-git.md#pushing-your-changes)
  - [Downloading new changes](4-using-git.md#downloading-new-changes)
  - [Submitting your changes](4-using-git.md#submitting-your-changes)
* [Asking for help](4-using-git.md#asking-for-help)


Set up necessary tools
----------------------

This section will tell you how to setup your copy of an engraving challenge repository.

### Install Git

You can download Git [here](http://git-scm.com/downloads).


### Haven't used command line before?

Check out [these tips](miscellaneous.md#using-command-line).


### Set up Git

Open the command line on your computer.  On Linux and MacOS, this will
probably be the "Terminal" app; on Windows, this will be the "Git Bash"
program installed with Git (_not the Windows command line_).

Tell Git your name and email, so that your work will be properly
attributed to you:

    git config --global user.name "Your Name Here"
    git config --global user.email "your_email@example.com"

(This may or may not be the same as the data used for creating a GitHub account.)


### Create an account on GitHub

Visit [github.com](http://github.com) website.



Set up the challenge
--------------------

### Fork the challenge's repository

Go to the GitHub page of the challenge's repository - they are listed [here](http://github.com/engraving-challenges) - and click `Fork` (in the upper-right corner).  This fork is *also* stored on GitHub, and you will have *write* access to it.


### Clone the repository to your computer

Open the command line, go to the directory into which you want to download the repository and run

    git clone https://github.com/USER_NAME/REPO_NAME.git

replacing USER_NAME with _your_ GitHub username, and REPO_NAME with challenge's repository name (e.g. `estrella`).

Git will create a new directory (named as the challenge's repository)
with a complete copy of your fork.


### Add upstream repository to your local clone

To be able to download new work submitted by other participants,
you have to add a _remote repository_.  In the command line, go
*inside your repository directory* and run

    git remote add upstream https://github.com/engraving-challenges/REPO_NAME.git

replacing REPO_NAME with the name of the challenge's repository.  This will add a remote named `upstream` that points to the challenge's official repository.



### Submit your first commit

This is a good way to check if everything is working correctly, and announce your participation in the challenge.

1. Create a subdirectory named "notationSoftware-yourName" (e.g. `Finale-2014-John-Doe`) in the repo.
2. Create an empty `README.md` file inside this subdirectory.
3. Tell Git to track this file with `git add *`.
4. Make a commit with `git commit -am 'New participant'`.
5. Upload your changes to your GitHub fork with `git push origin master`.
6. On your fork's GitHub webpage click `Compare & pull request` and then `Send pull request`.

If you're a bit confused, don't worry!  Next section explains everything in more detail.


Git crash course
----------------

Now it's the time to learn more about working with Git. If you are confused
or don't understand something, don't hesitate to ask on the [forum]
(http://engravingchallenges.freeforums.org/need-help-ask-here-f8.html).

### `git status` is your friend

As you will see throughout this manual, `git status` is a very useful command that will tell you a lot about the current state is your repository.  I used to run it literally before and after every other command, until I learned enough that I always knew what it will tell me.  In particular, it is a very good habit to run it after each commit - just to check whether all changes were commited succesfully.

Nice thing about this command is that it tells you what commands you can use to accomplish common tasks.


### Committing changes to the files

Open the [command line](miscellaneous.md#using-command-line) again,
go to your repository and run `git status`.  It should report

    On branch master
    [...]
    nothing to commit, working directory clean

The "nothing to commit, working directory clean" part means that the current state of the files in your repository folder is saved in Git's database.  In other words, you have no "unsaved changes".

Open the `README.md` file from your directory with a [text editor](miscellaneous.md#editing-text-files) and write something inside it - for example, introduce yourself briefly (remember to save changes in the modified file).  Then, go back to command line and run `git status` again.  This time it should tell something like this:

    [...]

    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   your-directory/README.md

    no changes added to commit (use "git add" and/or "git commit -a")

which means that Git detected that some files in the project were modified.  You can preview these changes using `git diff HEAD` (`HEAD` in Git means the latest commit) - this command will show you a "diff" between the current state of the file and the last saved version (if the diff is very long, you may have to press `q` to exit the "diff-preview" and go back to issuing normal commands).  Let's now commit the changes so that they are saved _in the repository_:

    git commit -am "Introduce myself"

The qouted text after "-am" is called "commit message". It is useful to put short information about commited changes here.

Now `git status` should again report "nothing to commit, working directory clean".


### Adding new files to the repository

Git only tracks changes in the files that were once "added" to the repository with `git add`.  In other words, if you just place a file inside the repository working directory and try to make a commit, Git won't look at that file.

Adding new files to the repo is very easy.  Create a new file (for example the `progress-report.md` file, or an empty file created with your notation software that will be filled with music from the challenge) and run `git status`.  It should list your file under "Untracked files":

    [...]

    Untracked files:
      (use "git add <file>..." to include in what will be committed)

            your-directory/your-new-file

    nothing added to commit but untracked files present

By the way, we recommend using dashes `-` instead of spaces in filenames.  Of course, Git can handle filenames with spaces, but using them on the command line is inconvenient.

To add your file to the repository, run `git add your-directory/your-new-file` (use [autocompletion](miscellaneous.md#using-command-line.md) to save typing).  You can also run `git add *` to add all untracked files at once.

Now, `git status` should report your file(s) under "Changes to be committed", and you can commit them.


### Important note about pdf files

When you modify a file and make a commit, Git will remember the new version of the file _together_ with all its previous versions.  Because of that you could just keep changing your score, overwriting the exported pdf file, and making a commit after each stage of work so that git will remember the state of your engraving file and pdf file at these moments.  All previous versions could then be loaded from Git database with the `checkout` command.

However, it would be inconvenient to have to go through all previous commits to see all versions of your score.  Therefore we ask you to create a **new** pdf file for each commit, so that it will be easier to view your progress (start the names of these pdfs with a number for better sorting).  _There is no need to create copies of your engraving file, though_ - so, each commit should consist of a _modification_ of your engraving file and a _new_ pdf file.


### Viewing your commits

To see your commits, use `git log` or `git log --oneline` commands.  They will show all commits, with the most recent ones on top.  Again, use `q` if necessary to exit the "log-viewer".  You may also use `--patch` option to view the changes that each commit introduced.  Note that this will be useful only with [plain text files](miscellaneous.md#plain-text) - if you have binary files, such as `.doc` or `.pdf`, there is no easy way to compare them and Git will just tell you that there was a change in such-and-such file.


### Pushing your changes

Use `git push origin master` to "upload" your changes to your GitHub fork (of course, you must be connected to the Internet to do this).  You will be asked for your GitHub username and password (note that nothing altogether will appear on the screen when you're typing your password, for security reasons).  After this you should be able to see your changes on the GitHub page of your fork.


<!-- Add later:
pay attention to "working dir clean"
which commands can be run with dirty tree:
whcih commands modify the state of the repository?
-->


### Downloading new changes

Remember that `upstream` remote repository we [added](4-using-git.md#add-upstream-repository-to-your-local-clone) to your local repo during setup?  Here's how to download new stuff from it.

Start by checking whether you have any uncommitted changes - use `git status`.  If it says "working directory clean", you're good to go.  If there are uncommitted changes (i.e. there are some files listed under "Changes not staged for commit", you should commit them to avoid the chance of running into trouble when downloading new changes.  If there are no uncommitted changes, but there are some untracked files, you may proceed, but it would be better to either commit or delete these files.

You may then push your work to your GitHub fork with `git push origin master`, just to have a backup in case something goes wrong (which is very unlikely).  Finally, run

    git pull upstream master

And that's it!  You should be able to see new commits using `git log` (or `git log --graph`), and the changes will be visible in your working directory.


### Submitting your changes

Start by downloading latest changes from the main repo, as described above.  Then, run

    git rebase upstream/master

to rearrange your commits a bit (this will make project history easier to follow).  After doing this, you have to push your changes to your GitHub fork - however, because of the rearranging performed above, you will most likely have to use `--force` option to do this.

**Important note:** be very careful when using `push --force`, because it can be dangerous.  `--force` means that Git will overwrite the destination branch on the remote repo with the contents of your local branch (in this case `master` branch), instead of just adding new commits.  If there were any commits in the destination branch that were not present in your local branch, they would be lost.  

Bearing this in mind, we do

    git push --force origin master

and the changes should land on your GitHub fork.  The last thing to do is to create a Pull Request.  On your fork's GitHub page, go to "Pull Requests" (on the right) and click "New pull request".  It should show your changes; after a quick check you can send the pull request by clicking the green **Create pull request** button.

You can read more about pull requests in [GitHub help](http://help.github.com/articles/using-pull-requests).


Asking for help
---------------

If you run into trouble or are not sure how to accomplish something, don't hesitate to ask us for help.  To ensure that we'll be able to help you, please don't just tell "I have a problem with adding files" but show what exactly you were doing, by copying and pasting from the command line.

Please include not only the error message, but also the command you issued (and maybe the previous one).  Output of `git status` can also provide us with helpful information.  If you include something like this:

    janek@pacan ~/engraving-challenges$ git status
    On branch master
    Your branch is up-to-date with 'origin/master'.

    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   LilyPond-devel/README.md

    no changes added to commit (use "git add" and/or "git commit -a")
    
    janek@pacan ~/engraving-challenges$ git add readme
    fatal: pathspec 'readme' did not match any files

then it should be easy for us to help you.


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`<= Git introduction`](3-git-introduction.md)
[`Main page`](README.md)
