**_Scores of Beauty_ Engraving Challenges**
[`Main page`](README.md)
[`Introduction`](1-goals-and-rules.md)
[`Editing workflow`](5-editing-workflow)
[`Forum`](http://engravingchallenges.freeforums.org)

-------------------------------------------

If you have not worked on projects that use Git, GitHub, and the Pull Request mechanism for collaborating, here is a brief overview of the basic concepts involved.  If you are already familiar with Git, feel free to skip this section.



What is version control?
------------------------

Version control is used to track how a set of files changes over time, and to manage these changes.  As a first approximation you may understand version control as an infinitely flexible undo/redo mechanism.

A version control system (VCS) stores the complete development history of your project and lets you investigate any state it has ever been in over time.

In Engraving Challenges we use Git as VCS, so the rest of this document is focused on it.


<!-- To be sorted out later:

http://git-scm.com/video/what-is-version-control

http://chronicle.com/blogs/profhacker/a-gentle-introduction-to-version-control/23064


Why use version control?
------------------------

Here are some of the reasons.  With version control, you can:
- you can have _thousands_ of savepoints without getting a headache
- restore your files to any of their previous versions
- you can easily revert mistakes
- it allows you to experiment freely with your project, without fear that you'll break something and won't know how to go back
- it gives you the power to inspect the history of your project
- collaborate more easily
- you don't have to remember what you;ve done ssince it will keep track of what you've done
- it gives *you* control over your files
- you can easily compare *any* past and present versions of the project
- you can easily see who and when made each and every change.
- including changes that made some problems
- spend less time discussing, and more doing. if others don't like your change, they can effortlessly revert it.
- you don't have to talk about every proposed change: make it, and ask others if they like it.  They can always revert it, or use only parts of it.
- you can very easily synchronize multiple copies of your project
- you can work dynamically, on multiple things in your project

"Version control is like accounting.  You could try to run a business
without it, and it may even work if the business is small. But you can
get lost or miss something important easily."

"Version control is like insurance.  Would you go to safari or
mountain trip without an insurance?  Sure, usually nothing bad will
happen to you... but when it does happen, you will be very sorry"

**If it's so great, why isn't everybody using it?**
Most people don't know about it.  Those who do often don't realize that it could be useful for them, or they think it's too hard.
It takes some timee to learn how to use it effectively, but it's not particularly hard.

-->


Git Basics
----------

### Repositories

A project usually has one main repository ("repo"), stored on GitHub (or other similar service) - which reflects the "official" state of the project.  This repository is used as the basis for other repositories that individual contributors may maintain, both on GitHub and on their own local machines.  It is customary to refer to this main repository as the "upstream" repo.

This repo is what you will *read* from whenever you need to get the latest versions of the project files.  All your changes should also finally land there, but you will probably not write to this repo directly - the project lead(s) will merge your changes when you sumbit them.

When you join a project, you start by creating your own copies of the main repo.  Firstly, you create a "fork" on GitHub - this repository will be visible to other people, and you will have *write* access to it.  You will then "clone" this fork to your computer; we will refer to this copy as the "local clone" or "local repo".  This local repo remembers the adress of your fork as a "remote" repository called `origin`.

Repositories can talk to each other.  Uploading changes from local repository to remote repository is called "pushing", and downloading changes from remote repo is called "pulling" or "fetching".  Any repository can talk to any other repository (i.e. changes can be sent between any repos), but usually changes travel between repos in a specific order.

Changes in one repository aren't automatically transferred to other repositories.  In particular, new work submitted by other contributors to the main repo won't be automatically copied to your GitHub fork, nor downloaded to your local repo.


### Workflow Overview

#### Working on local copy

Most of the time you'll be working with your local repo, which is your own personal sandbox.  You can play with these files however you like - in particular, you can create new files and tell Git to track them.

Every so often, you'll decide that you want to make a snapshot of the current state of your work.  This is called a "commit".  Making a commit is similar to saving a document after making some modifications, except that when you save a document, it's previous version is overwritten - but when you make a new commit, all previous commits will remain available in your repository.

After one or more of these commits, you can upload ("push") them to your fork on GitHub.  This has two purposes: first, you will have a backup of your work; second, other people will be able to see what you've done.

#### Uploading your work

When you decide that you have finished a coherent set of changes and would like to submit them to the official repo, you once again upload your changes to your GitHub fork and then issue a Pull Request to ask the project lead to merge your changes into the upstream repo.

You will also periodically grab the work others have submitted by pulling changes from upstream repository.  After doing so, you can continue working, do more commits, more pushes, and pull requests, and the cycle continues.

This basic overview applies to many projects on GitHub.  In the next section, you'll find some more specific information on working with Engraving Challenges repositories.


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`Main page`](README.md)
[`Introduction`](1-goals-and-rules.md)
[`Editing workflow`](5-editing-workflow)
[`Forum`](http://engravingchallenges.freeforums.org)
