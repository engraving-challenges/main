**_Scores of Beauty_ Engraving Challenges**
[`Main page`](README.md)
[`Introduction`](1-goals-and-rules.md)
[`Editing workflow`](5-editing-workflow.md)
[`Forum`](http://engravingchallenges.freeforums.org)

-------------------------------------------


Downloading new changes
-----------------------

Remember that `upstream` remote repository we [added](3-setup.md#add-upstream-repository-to-your-local-clone) to your local repo during setup?  Here's how to download new stuff from it.

Start by checking whether you have any uncommitted changes - use `git status`.  If it says "working directory clean", you're good to go.  If there are uncommitted changes (i.e. there are some files listed under "Changes not staged for commit", you should commit them to avoid the chance of running into trouble when downloading new changes.  If there are no uncommitted changes, but there are some untracked files, you may proceed, but it would be better to either commit or delete these files.

You may then push your work to your GitHub fork with `git push origin master`, just to have a backup in case something goes wrong (which is very unlikely).  Finally, run

    git pull upstream

And that's it!  You should be able to see new commits using `git log` (or `git log --graph`), and the changes will be visible in your working directory.


Submitting your changes
-----------------------

Start by downloading latest changes from the main repo, as described above.  Then, run

    git rebase upstream/master

to rearrange your commits a bit (this will make project history easier to follow).  After doing this, you have to push your changes to your GitHub fork - however, because of the rearranging performed above, you will most likely have to use `--force` option to do this.

**Important note:** be very careful when using `push --force`, because it can be dangerous.  `--force` means that Git will overwrite the destination branch on the remote repo with the contents of your local branch (in this case `master` branch), instead of just adding new commits.  If there were any commits in the destination branch that were not present in your local branch, they would be lost.  

Bearing this in mind, we do

    git push --force origin master

and the changes should land on your GitHub fork.  The last thing to do is to create a Pull Request.  On your fork's GitHub page, go to "Pull Requests" (on the right) and click "New pull request".  It should show your chages; after a quick check you can send the pull request.

You can read more about pull requests in [GitHub help](http://help.github.com/articles/using-pull-requests).


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`Main page`](README.md)
[`Introduction`](1-goals-and-rules.md)
[`Editing workflow`](5-editing-workflow.md)
[`Forum`](http://engravingchallenges.freeforums.org)
