**_Scores of Beauty_ Engraving Challenges**
[`Main page`](README.md)
[`Using Git`](4-using-git.md)

-------------------------------------------


### Using command line

The command line is a way of communicating with your computer.  It allows you to communicate with computers more directly than using a mouse.

Here are a few tips to get you started:

- When you open the command line for the first time, all you can see is the
  "prompt", which looks like `username@hostname ~/where/you/are $`.
  To run a command, just type it and press `ENTER`.  The command will usually
  produce some output, and then a new prompt will appear.

- The `~/where/you/are` bit in the prompt is called "current working directory".
  All commands you run are executed from that directory.  This is actually quite
  similar to how you usually work with your computer - when you turn it on, you
  can see your desktop and the files that are on it.  To see files that are in
  some other folder, you open that folder.  You can operate on the files that
  you can see in the currently opened folder - just like current working directory.

- To see all files and directories in the current working directory, use `ls` or `ls -l`.

- To go to some other directory, use `cd path/where/you/want/to/go`  
  (note that this path is relative to the directory you're currently in.)

- To go to the parent directory, use `cd ..`.

- If you want to use filenames with spaces and similar special characters,
  you have to use quotes, like this: `cd "folder with spaces in name/subdirectory"`

- Save typing by using autocompletion.  After writing a few initial characters
  of a command (or a path, etc.) press `TAB` to have it automatically completed.
  If there are more than one possibility to complete the command nothing will happen
  first, but pressing `TAB` a second time will present you with a list of all
  possible completions.

- On Linux and MacOS copying and pasting in command line is usually done
  with `Ctrl-Shift-C` and `Ctrl-Shift-V` (instead of `Ctrl-C` and `Ctrl-V`).
  On Windows, pasting is done with `Insert` key.

- pressing `Ctrl-C` in command line tells the computer to abort the command
  that is currently being executed, so you usually don't want to press this
  key combination accidentally :-)

_Back to [using Git](4-using-git.md)_


### Editing text files

Don't use word processors (like Microsoft Word or OpenOffice) to edit plain text files - it's like driving a truck to take your kids to school.  Instead, use a _text editor_ such as TextMate (on MaxOS), Notepad++ (on Windows), JEdit (on any operating system) or some other.

Note that Windows notepad _isn't_ a reasonable text editor (it doesn't work well with some files) - you have to use something else.  It seems that Microsoft doesn't think that their operating system should include a decent text editor...

_Back to [using Git](4-using-git.md)_


### What are `.md` files?

`.md` files are [plain text](miscellaneous.md#plain-text) files (similar to `.txt` files) with formatting in [Markdown](http://en.wikipedia.org/wiki/Markdown).  Many websites like GitHub can display Markdown-formatted files nicely formatted.  You can edit these files with [any text editor](miscellaneous.md#editing-text-files).


### Plain text

We say that data is stored in plain text files if these files are human-readable.  In other words, when you open a plain text file in a text editor you will see _text_.  If you see garbage, like this: `xڭ\I#???|vܗɐЏL???????FV&Y\mUe6OKҡ` then it's not a plain text file.

`.txt` and `.md` files are examples of plain text formats.

Plain text files don't require special software to be read and written; they are easy to process.  To get the idea of the difference between plain text files and binary files (such as `.doc` or `.pdf` files), imagine that you have the following two methods to record a piece of text (a poem, or a shopping list):
* writing it down on paper using a pencil,
* using a special machine that chemically imprints the text on a thick metal plate in such a way that it can only be seen when the plate is freezed.

The first method is cheaper, you don't need specialistic tools for it, you may read the text any time you wish, and the paper is easier to carry around.  And if you have a rubber and a pencil (or a pen, or a crayon), you can modify the text as you wish.

The second method... well, it's only advantage is that the machine can produce the prints in color, and they have high resolution.  But the fact that you have to carry a refridgerator with you just to read them doesn't make it very convenient.


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`Main page`](README.md)
[`Using Git`](4-using-git.md)
