THIS FILE SHOULD BE MOVED TO GIT-INTRODUCTION REPO
(once we finish the reorganization)


### on cloning 

Yeah, git assumes you want to create a new directory with the repository's name if you don't tell it otherwise.

You can specify the path where the cloned repository should be put, like this:
git clone https://github.com/blahblah/blahblah path/where/the/stuff/should/be/put

This way you don't even have to be in the directory were the clone will be placed (the directory may not even exist yet).


### git status

will tell you what to do.


### adding files and ignored files

>     There's one  gotcha here: git has a list of filetypes it ignores in the .gitignore file,
>     and by default .pdf is on this list - so if you're wanting to track and
>     upload PDFs you'll need to edit .gitignore and get rid of the pdf entry.


This may not be a good idea: the .gitignore is part of the repository (git actually tracks it).  You should rather add the file explicitely, i.e. 'git add filename' (without using wildcards).


### clean working directory

Akin to unsaved changes in an opened file.  You wouln't shut your computer down in such situation.