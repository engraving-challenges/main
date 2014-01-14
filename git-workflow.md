## Git Workflow

If you are already proficient with Git you'll find concise information
about how we want you to work with the Git repository her.
Feel free to ask for any clarification or details.

If you're new to that you may skip this document and rely on personal
communication with someone who helps you out.

1. **Accounts**   
   If you don't already have one, get yourself a Github account
   and fork this repository. In general participants won't have
   push access to the main repository but add their contributions
   through the `Pull request` interface.
2. **Branches**  
   The `master` branch is intended to reflect the overall progress
   of the project. Actually this branch should only move forward
   when merging in a completed challenge.  
   For each challenge a base develop branch is used, and any concrete
   work should be done on feature branches created off the challenge
   branch.   
   If in any doubt ask someone to set up a working branch for you.
3. **Merging**  
   We want a clean history that is nevertheless informative about the
   way of progress. Therefore usually branches should be `rebase`d
   before being merged *with merge commit* (through the `--no-ff`
   option.  
   If you don't consider yourself an administrator of this repository
   you should *not* merge branches yourself but rather open a pull
   request (after having rebased).  
   Once you have completed a coherent step of your assignment
   you should rebase your working branch against the challenge's
   base branch and merge or open a pull request.
4. **Commit strategies**  
   Please commit very often. We're particularly interested in the detailed
   documentation of the progress, therefore we need this information.  
   In general commit any individual modification or coherent set of
   changes. This may for example be the addition of a complete voice,
   the definition of a page layout or (later in the project) a single
   fixed pitch or positioning. We know that with binary files this will
   bloat the size of the repository because binary files aren't really
   suitable to be version controlled, but we'll accept this for the sake
   of transparency.  
   Use commit messages to leave as many information as possible about
   what you did. You can also use them to store timing information.  
   Please don't exceed 50 characters for the message header and 80
   characters for the message body. Use hard line breaks and avoid
   whitespace at line ends.
5. **Tracking PDFs**  
   As a convenience we also track PDF files, which makes it easier to
   create a report of the progress (we can't generate PDFs from
   arbitrary states of your document files when they're not created with
   Free Software). By default PDF files are ignored by the repository,
   so you should manually stage the PDF file to add it to the repository.  
   If you use LilyPond or another free tool that allows us to recreate
   PDFs from any given state you should not commit *every* change of the
   PDF files but only relevant states (while you are encouraged to commit
   the changes to the actual document files as often as possible).

---

Back to the [Contributor's Guide](README.md)
