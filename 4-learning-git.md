**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](3-setup.md)
[`main page`](README.md)
[`next =>`](5-editing-workflow.md)

-------------------------------------------


Working with Git
----------------

### Committing changes to the files

Now it's time to learn more about working with Git.  Open the command line again, go to your repository and run `git status`.  It should report

    On branch master
    [...]
    nothing to commit, working directory clean

The "nothing to commit, working directory clean" part means that the current state of the files in your repository folder is saved in Git's database.  In other words, you have no "unsaved changes".

Open the `README.md` file from your directory with a [text editor](miscellaneous.md#editing-text-files) and write something inside it - for example, introduce yourself briefly.  (Remember to save changes in the modified file.)  Then, go back to command line and run `git status` again.  This time it should tell something like this:

    [...]

    Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   your-directory/README.md

    no changes added to commit (use "git add" and/or "git commit -a")

which means that Git detected that some files in the project were modified.  You can preview these changes using `git diff HEAD` (`HEAD` in Git means the latest commit) - this command will show you a "diff" between the current state of the file and the last saved version.  (If the diff is very long, you may have to press `q` to exit the "diff-preview" and go back to issuing normal commands.)  Let's now commit the changes so that they are saved _in the repository_:

    git commit -am "Introduce myself"

Now `git status` should again report "nothing to commit, working directory clean".


### Adding new files to the repository

Git only tracks changes in the files that were "added" to the repository with `git add`.  In other words, if you just place a file inside the repository working directory and try to make a commit, Git won't look at that file.

Adding new files is very easy.  Create a new file (for example it can be an empty file created with your notation software, which you will later fill with music from the challenge) and run `git status`.  It should list your file under "Untracked files":

    [...]

    Untracked files:
      (use "git add <file>..." to include in what will be committed)

            your-directory/your-new-file

    nothing added to commit but untracked files present

By the way, we recommend using dashes `-` instead of spaces in filenames.  Of course, Git can handle filenames with spaces, but using them is inconvenient.

To add your file to the repository, run `git add your-directory/your-new-file` (use [autocompletion](using-command-line.md) to save typing).  You can also run `git add *` to add all untracked files at once.

Now, `git status` should report your file(s) under "Changes to be committed", and you can commit them.


### Viewing your commits

To see your commits, use `git log` or `git log --oneline` commands.  They will show all commits, with the most recent ones on top.  Again, use `q` if necessary to exit the "log-viewer".  You may also use `--patch` option to view the changes that each commit introduced.  Note that this will be useful only with [plain text files](miscellaneous.md#plain-text) - if you have binary files, such as `.doc` or `.pdf`, there is no easy way to compare them and Git will just tell you that there was a change in such-and-such file.


### Pushing your changes

Use `git push origin master` to "upload" your changes to your GitHub fork.  (Of course, you must be connected to the Internet to do this.)  You will be asked for your GitHub username and password (note that nothing altogether will appear on the screen when you're typing your password, for security reasons).  After this you should be able to see your changes on the GitHub page of your fork.


<!-- Add later:
pay attention to "working dir clean"
which commands can be run with dirty tree:
whcih commands modify the state of the repository?
-->


### `git status` is your friend

As you probably noticed, `git status` is a very useful command that will tell you in what state is your repository.  I used to run it literally before and after every other command, until I learned enough that I always knew what it will tell me.

Nice thing about this command is that it tells you what you could do, for example how to add files to the repository.


### Asking for help

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
[`<= previous`](3-setup.md)
[`main page`](README.md)
[`next =>`](5-editing-workflow.md)
