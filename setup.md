_This guide assumes that you are new to Git and version control.
If you already know these tools, see the [Advanced guide]()._

Setup
-----

0. [**Read an introduction about Git**.]
   (https://github.com/openlilylib/git-introduction/blob/master/old-git-basics.md)

1. **[Install Git](http://git-scm.com/downloads)**

2. **Set up Git**
   - Open the command line on your computer.  On Linux and MacOS, this will
     probably be the "Terminal" app; on Windows, this will be the "Git Bash"
     program installed with Git (_not the Windows command line_).
   - Tell Git your name and email, so that your work will be properly
     attributed to you:
     
     ``` bash
     git config --global user.name "Your Name Here"
     git config --global user.email "your_email@example.com"
     ```

3. **Haven't used command line before?** A few tips:  
   - When you open the command line for the first time, all you can see is the
     "prompt", which looks like `yourusername@hostname ~/where/you/are $`.
     To run a command, just type it and press `ENTER`.  The command will usually
     produce some output, and then a new prompt will appear.
   - The "~/where/you/are" bit in the prompt is called "current working directory".
     All commands you run are executed from that directory.  This is actually quite
     similar to how you usually work with your computer - when you turn it on, you
     can see your desktop and the files that are on it.  To see files that are in
     some other folder, you open that folder, and you can operate on the files that
     you can see in the currently opened folder.     
   - To see all files and directories in the current working directory, use `ls`.
   - To go to some other directory, use `cd path/where/you/want/to/go`.
   - To go to the parent directory, use `cd ..`.
   - If you want to use filenames with spaces and similar special characters,
     you have to use quotes, like this: `cd "folder with spaces in name/subdirectory"`
   - Save typing by using autocompletion.  After writing a few initial characters
     of a command (or a path, etc.) press `TAB` to have it automatically completed.
   - Copying and pasting in command line is usually done with `Ctrl-Shift-C` and
     `Ctrl-Shift-V` instead of `Ctrl-C` and `Ctrl-V`.
   - pressing `Ctrl-C` in command line tells the computer to abort the command
     that is currently being executed, so you usually don't want to press this
     key combination accidentally :)

4. **Create an account on [GitHub](github.com)**

5. **Fork the challenge's repository**  
   On the GitHub website, find the repository with the challenge that you
   want to work on (they are listed [here](github.com/engraving-challenges))
   and click `Fork` (in the upper-right corner).

6. **Clone the repository to your computer**  
   Open the command line again, [navigate](tips)
   to the directory where you want to place the repository and run
   `git clone https://github.com/USER_NAME/REPO_NAME.git`,
   replacing "USER_NAME" with your GitHub user name, and "REPO_NAME"
   with the actual name of the challenge's repository. 
   (You may also copy the repository address from GitHub.  On the website
   _of your fork_, find the `HTTPS clone URL` - it's located on the right).

7. **Add upstream repository to your local clone**
   To be able to download any new work submitted by other participants,
   you have to add a _remote repository_.  In the command line, run
   `git remote add upstream https://github.com/engraving-challenges/REPO_NAME.git`,
   replacing "REPO_NAME" with the name of the challenge's repository.    
   