**_Scores of Beauty_ Engraving Challenges**
[`back to main page`](http://github.com/engraving-challenges/main/)

-------------------------------------------


This section is not meant to be read all at once.  Rather, use it as a reference, looking up things that are not clear for you.

### git clone

`git clone <remote repository address>` will create a new directory (named the same as the cloned repository) in the current directory.  So, if you are in directory `~/music/engraving/` and you run `git clone https://github.com/github-user-name/foobar.git`, git will clone the repository into `~/music/engraving/foobar`.

You can also specify the path where the cloned repository should be put, like this:
`git clone <remote repository address> <destination path>

If the <destination path> doesn't exist, it will be created.

Please note that `git clone` will create a subdirectory inside your current
working directory, so you don't need to create a directory for the new
repository. Instead you should have something like a base directory where
you want to store all your repositories in and run `git clone` from there.
This will download a copy *of your fork* to your local disk and initialize
it as a Git repository.


### remote repository

A remote repository is a repository external to this one (UGH).  It usually is placed in the Internet.

`git remote --verbose`

### working directory

TODO


### "working directory clean"

Clean working directory means that the current state of the files in the working directory is saved (committed) to the repository.  To better understand this, imagine that you open a document in an editor.  If you make some changes but don't save the file, 
Akin to unsaved changes in an opened file.  You wouln't shut your computer down in such situation.


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`back to main page`](http://github.com/engraving-challenges/main/)
