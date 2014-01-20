**This fille will go back to the git-introduction repo once i'm done with it.  Just wanted to have stuff in one place.**

This document had originally been written as part of the openLilyLib engraving challenges.
Here it is simply copied to be available. But we'll pick the pieces from it and move them
to appropriate places in other documents when developing our Git Introduction.

# Git Basics

If you have not worked on projects that use Git, GitHub, and the Pull Request mechanism for collaborating, here is a brief overview of the basic concepts involved.  You will also find much more information on Git from [the free Git Book] (http://git-scm.com/book).  You will also find more specific information on the workflow employed by this particular project in [the Git Workflow document](git-workflow.md).

## Repositories

A project has a main repository ("repo") stored somewhere on the Internet - usually on GitHub.  This is the public face of the project and is where the files accessible to everyone are stored.  It is used as the basis for other repositories that individual contributors may maintain, both on GitHub and on their own local machines.  It is customary to refer to this main repository as the "upstream" repo.

This repo is what you will *read* from whenever you need to get the latest and greatest versions of the project files.  You will probably not write to this repo directly; only the project lead(s) will do this.

When you first join a project, you start by creating your own copy of that repo.  This fork is *also* stored on GitHub, and you will also have *write* access to this copy.
You will then have to create a local "clone" of the repository where you can work with on your computer.

A remote repository is a repository external to this one (UGH).  It usually is placed in the Internet.

Now you have a local repository and a `remote` repository. Cloning has automatically registered your fork on GitHub as a remote called `origin`. From this remote you can always `pull` or `fetch` data (i.e. download to your local repository) or `push` (i.e. upload to the remote repository).

One more thing to note is that forking creates a *copy* of the original repo, but further changes on the original will *not* be visible on the fork by default.  In order to overcome this you will establish a connection to the 'official' repo by adding it as an additional remote, customarily called `upstream`. You will be able to download new work from there to update your local repo.

## Workflow Overview

It is the local repo on your own machine you will be working on mostly.  When you want to make your work available to others, you will upload your changes to your origin repo on GitHub and then issue a Pull Request to ask the project lead to merge your changes into the upstream repo.  Once your changes have been merged into the upstream repo, they become available to others.  You will also periodically update your own local repo from the upstream repo to incorporate others' changes.

Your local repo is your own personal sandbox.  You can play with these files however you like, including adding new ones.  

Every so often, you decide things are at a state where you want to take a snapshot of your current sandbox to record the current state of your work for posterity.  You do this via `git commit`.  After one or more of these commits, you might decide you are at a point where you feel these should be written to your fork on GitHub, so you do a `git push`.  After one or more of these pushes, you might decide your work is ready to be shared with others, so you visit your fork on GitHub and press the `Pull Request` button to ask the project leads to merge your changes into the main (upstream) repo.

Every so often, you will also decide it would be good to grab the work others have been contributing.  So you do a `git fetch upstream` to download the latest version of everything.  Because of the details of how git manages version control, you have to also do a `git rebase` or `git merge` to fully incorporate these downloaded changes into your local repo.  This is the step hardest to fully grasp, I find, but do not worry at this point about the specifics of what this does.  Once you have updated your local repo, you can continue working, do more commits, more pushes, and pull requests, more fetches, and the cycle continues.

You will normally create "branches" for your work, but the rules for how you are expected to manage your branches may differ from project to project.  That is where the [git workflow](git-workflow.md) for your specific project will hopefully give you more guidance.

Again, this basic overview applies to many projects on GitHub.  For more information on the workflow for this specific project, including when and how to branch, commit, push, and issue Pull Requests, see the [Git Workflow document](git-workflow.md).
