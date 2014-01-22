**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](3-setup.md)
[`main page`](http://github.com/engraving-challenges/main/)
[`next =>`](5-editing-workflow.md)

-------------------------------------------

Use `git status` all the time

pay attention to "working dir clean"

which commands can be run with dirty tree:
whcih commands modify the state of the repository?

## Initial Setup

Before you begin, you will need to create an account on [GitHub](https://github.com).  You will also need to install [Git tools](http://git-scm.com/downloads) on your own machine.


### What's the situation:


main repo
fork
local


### git status

a bit of git advice: git status is your best friend.  I used to run it literally before and after every other command, until i learned enough that i always knew what it will tell me.


### more on adding, and on troubleshooting

The first thing to do is to navigate to the directory where your repository is (on your computer) - use 'git bash' program and 'cd' command for this.  And run 'git status' - this is the most important command of all, you want to run it all the time to see what is happening.  It should provide us with info that will enable us to troubleshoot your problem.  What does 'git status' tell?

Another thing: please always, **always** paste not just the error message, but also the exact command you issued (and maybe the previous one) into your emails.  Something like this:

> janek@pacan ~$
> cd ~/repos/lilypond-git
> janek@pacan ~/repos/lilypond-git (master)$
> git status
> On branch master
> Your branch is up-to-date with 'origin/master'.

> Changes not staged for commit:
>   (use "git add <file>..." to update what will be committed)
>   (use "git checkout -- <file>..." to discard changes in working directory)

>     modified:   lily/parser.yy

> Untracked files:
>   (use "git add <file>..." to include in what will be committed)

>     input/regression/event-listener-output-violin-1.notes
>     input/regression/event-listener-output.pdf

> no changes added to commit (use "git add" and/or "git commit -a")
> janek@pacan ~/repos/lilypond-git (master)$
> git add foooooooo
> fatal: pathspec 'foooooooo' did not match any files
> janek@pacan ~/repos/lilypond-git (master)$

It's the only way for us to know what you're actually doing so that we may guess why it fails.


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](3-setup.md)
[`main page`](http://github.com/engraving-challenges/main/)
[`next =>`](5-editing-workflow.md)
