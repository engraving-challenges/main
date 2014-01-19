_This guide assumes that you are new to Git and version control.
If you already know these tools, see the [Advanced guide]()._

Set up necessary tools
----------------------

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

**Question: Does this have to be the same email as used for the Github account?**

### Haven't used command line before?

A few tips:

- When you open the command line for the first time, all you can see is the
  "prompt", which looks like `username@hostname ~/where/you/are $`.
  To run a command, just type it and press `ENTER`.  The command will usually
  produce some output, and then a new prompt will appear.

- The `~/where/you/are` bit in the prompt is called "current working directory".
  All commands you run are executed from that directory.  This is actually quite
  similar to how you usually work with your computer - when you turn it on, you
  can see your desktop and the files that are on it.  To see files that are in
  some other folder, you open that folder.  You can operate on the files that
  you can see in the currently opened folder - just like current working directory.

- To see all files and directories in the current working directory, use `ls` or `ls -l`.

- To go to some other directory, use `cd path/where/you/want/to/go`  
  (note that this path is relative to the directory you're currently in.)

- To go to the parent directory, use `cd ..`.

- If you want to use filenames with spaces and similar special characters,
  you have to use quotes, like this: `cd "folder with spaces in name/subdirectory"`

- Save typing by using autocompletion.  After writing a few initial characters
  of a command (or a path, etc.) press `TAB` to have it automatically completed.
  If there are more than one possibility to complete the command nothing will happen
  first, but pressing `TAB` a second time will present you with a list of all
  possible completions.

- Copying and pasting in command line is usually done with `Ctrl-Shift-C` and
  `Ctrl-Shift-V` instead of `Ctrl-C` and `Ctrl-V`.

- pressing `Ctrl-C` in command line tells the computer to abort the command
  that is currently being executed, so you usually don't want to press this
  key combination accidentally :-)



Set up the challenge
--------------------

### Fork the challenge's repository

On the GitHub website, find the repository with the challenge that you
want to work on (they are listed [here](github.com/engraving-challenges))
and click `Fork` (in the upper-right corner).


### Clone the repository to your computer

Open the command line again, [navigate](setup.md#havent-used-command-line-before)
to the directory where you want to place the repository and run
`git clone https://github.com/USER_NAME/REPO_NAME.git`,
replacing USER_NAME with your GitHub user name, and REPO_NAME
with the actual name of the challenge's repository.
(You may also copy the repository address from GitHub.  On the website
_of your fork_, find the `HTTPS clone URL` - it's located on the right).  
Please note that `git clone` will create a subdirectory inside your current
working directory, so you don't need to create a directory for the new
repository. Instead you should have something like a base directory where
you want to store all your repositories in and run `git clone` from there.
This will download a copy *of your fork* to your local disk and initialize
it as a Git repository.


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

Create a subdirectory for yourself, with the name "notation-software-your-name" (for example `Finale-2014-John-Doe` - remember to include software version).  Inside, create a `README.md` file (`.md` files are similar to `.txt` files).  In this file you may introduce yourself briefly.

Run `git status` again - it should now list your directory under "Untracked files".  Use `git add your-directory-name` to tell git to start tracking it, and make a commit with `git commit -a`
