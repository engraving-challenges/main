## Git Workflow

This document provides a concise description of our Git workflow.
It is not intended to introduce you to Git's concepts or tell you
how to achieve a specific task. If you're having problems to understand
or do this please contact us or visit our (work-in-progress)
[Git introduction](https://github.com/openlilylib/git-introduction).

1. **Accounts**   
   If you don't already have one, get yourself a Github account
   and fork the challenge's repository. In general participants won't
   have push access to the main repository but add their contributions
   through the `Pull request` interface.
2. **Clone and remotes**  
   Create a local clone of your fork and add
   `https://github.com/engraving-challenges/CHALLENGE.git` -
   replacing "CHALLENGE" with the actual name of the challenge's
   repository.  
   Please always do `git fetch upstream` to download any new work
   by other contributors.
4. **Pull requests**  
   Whenever you have finished some coherent amount of work (e.g. entering
   the plain music, apply beautification, proof-reading) you should open
   a pull request. Before doing so please update your working branch with  
   `git pull upstream`  
   `git rebase upstream/master`.  
   This will download all work from others and create a clean history for us.
5. **Commit strategies**  
   Please commit very often. We're particularly interested in the detailed
   documentation of the progress, therefore we need this information.
   In general, commit any individual modification or coherent set of
   changes. This may for example be the addition of a complete voice,
   the definition of a page layout or (later in the project) a single
   fixed pitch or positioning. We know that with binary files this will
   bloat the size of the repository because binary files aren't really
   suitable to be version controlled, but we'll accept this for the sake
   of transparency.  
   Use commit messages to leave as much information as possible about
   what you did. You can also use them to store timing information.
   Please make the title of the commit (the "Commit summary" on Github's
   website) as clear as possible because that's what one will see when
   browsing the project history.
   Please don't exceed 50 characters for the message header and 80
   characters for the message body. Use hard line breaks and avoid
   whitespace at line ends.
5. **Tracking PDFs**  
   As a convenience we also track PDF files, which makes it easier to
   create a report of the progress (we can't generate PDFs from
   arbitrary states of your document files when they're not created with
   Free Software). 
   If you use LilyPond or another free tool that allows us to recreate
   PDFs from any given state you should not commit *every* change of the
   PDF files but only relevant states (while you are encouraged to commit
   the changes to the actual document file itself as often as possible).

---

Back to the [main page](README.md)
