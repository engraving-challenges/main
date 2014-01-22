**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](4-learning-git.md)
[`main page`](http://github.com/engraving-challenges/main/)
[`next =>`](6-collaboration.md)

-------------------------------------------

# General Challenge Rules / Contributor's Guide

If you participate in an **_Scores of Beauty_ Engraving Challenge** you should
try to follow the workflow described in this document as closely as
possible. We've set it up in order to provide a working situation that
offers the best possible basis for comparison of different tools'
strengths and weaknesses.  
However, if some of these guidelines come severely across the way your
tool suggests you to work, then you can of course deviate. But please
do so with enough documentation so we can see your reasoning (and learn
something about your tools).

---

### Set-up:

You are encouraged to add any number of
Markdown files (possibly in a subdirectory) to make notes, either for
your personal use or for documentation, but in the end you should have one
README.md file in "your" root directory that serves as the main
documentation of your attempt.

Finally your "root" directory should contain your main (or entry-point)
document file and the resulting PDF file.

---
For the purpose of our challenges it is
important to make this as concise and fine-grained as possible.  
If you don't have experience with Git and aren't in the position to
learn it for this occasion, don't worry. You can ask someone to assist
you with that.

   
### Project Phases

Please tackle your assignment according to the following outline. You
may deviate from this order if there are compelling reasons,
but please do only after reporting back that you are going to do so,
and of course with appropriate documentation. As an example it may make
sense to temporarily modify page layout for proof-reading.

#### Analyze the task

Have a close look at the assignement and the given score. Please make
notes about your impressions: How do you expect your tools to be able
to deal with the task, which problems do you expect, do you think
about a specific approach etc.?

#### Music Entry

In a first step please enter the absolute "raw material". That is,
simply set up your score with the necessary information about parts etc.
but do *not* make any adjustments to the layout or appearance (the only
exception to this rule might be if an assignment would result in a score
that doesn't fit on standard paper). The idea is to get an impression
of the out-of-the-box output of the different tools.

Even more important: do *not* apply *any* individual adjustment or tweak
to improve the output quality, it has to be the plain content that is entered.
What is of course accepted (and encouraged) is the correct
assignment to voices (or layers). Also accepted *(but only if 
documented)* are "on/off" operations like manually switching directions or breaking beams etc.

If your prior analysis has shown that you need specific functionality,
for example through the use of plugins or functions, to fulfill specific
demands of the given score, and that it would be nonsensical to apply
this only *after* music entry, you may prepare this before the music
entry itself (again only with appropriate documentation). Again, this
isn't a licence for manual tweaks to overcome limitations of the used
tools.

#### Proof-reading / Peer review

Now the entered music should be proof-read. We can't prescribe too
specific workflows for this phase because they might differ between
the used tools. The only thing we require this to be done through
peer-review. That is, someone else has to proof-read the score. It is
up to you if you find a usable Git based solution or if you send a
printout by postal mail, just do it collaboratively and make notes
about your solutions.

#### Global Layout and Appearance

Once the music is entered and we've seen the default output of your
program you can adjust the global appearance setting in any way you
like. You may adjust page layout, staff and font sizes, line thicknesses
or whatever to realize your "house style". If you want you can now
also decide about line and page breaking.  
Please do these things in retraceable steps and commit any sensible unit
of work. If your document files don't "speak for themselves" through
Git diffs please document each step meticulously.  
Again, in this phase you're not allowed yet to tweak any object
individually.

#### Tweak to Usable Quality

For many applications you don't need publication quality scores, the most
common being the use as performance material. We are interested in the
amount of work to bring a score to such a state with different tools.
(Of course we know that the state of 'usable quality' is a highly subjective
one.)

#### Tweak to Publication Quality

Now you should make your score perfect. You're allowed to use *any*
tools your program offers, including third-party plugins, self-written
functions or established libraries. But anything has to be reproducible
by others. This means that if your score requires a - commercial or free -
plugin or library to be present this fact has to be documented.
If you use functions or self-written tools
that aren't publicly available they have to be somehow accessible
(for LilyPond you can either place them in the input files themselves,
in directories reachable from the main file or in a library directory
that we can put into the repostory if necessary).  
As usual all steps should be documented verbally and/or through Git
commits.

#### Final Proof-reading

A last round of proof-reading should also be made with peer-review.
This should be interested in errors regarding the content as well as
engraving shortcomings. Here it is specifically important to commit
each modification individually as we're very interested in the impact
such fixes will have on an already beautified score.
So, if adjusting a dynamic makes a slur move and collide with something else,
please make a commit in that state and then a separate commit for fixing
the collision that ensued.

## Commit strategies

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

GIT Editing cycle
-------------

edit files

if you created new files, add them with `git add`.

Commit

push


### by Janek:
* ask participants to measure time spent on each step, to judge which program is faster
* asking in general "please commit often, so that we can see each stage of the project's progress" does not work very well, because the number of commits people make varies wildly (someone did the whole thing in 3 commits, another in 30, and another had 10 commits just for note entry).  Instead, state the number of expected commits (i think this should be 5-10 for simple pieces and 15-30 for complex ones) and try to list all stages when one's expected to make a commit.  It might be a great help to first typeset the challenge ourselves so that we can see where the commits should be.
* track *all* pdfs, so that we can afterwards see *every* step.  After all, pdfs are usually 20-100 kB in size, so it shouldn't be too much (100kB * 20 commits = 2 MB per participant, that's not much).
* as for tracking pdfs (and maybe other binary files): this won't be very "gitish", but i suggest that a new file should be added for every commit (instead of replacing previous file), so that when one checks out the tip of the branch, he can see all stages of work without having to checkout every commit separately.  (Example: sth like what [David Webber did with Mozart](https://github.com/MozartSoftware/engraving-challenges/tree/e3119af366d7bb43ac965286ac2104be981d17dd/challenge02-schumann/Mozart))
* it seems that some people don't actually commit their program's files (`.mus`, `.sib` etc - whatever their program uses)!  We must emphasize that it's crucial to do this, as we want to be able to reproduce the steps (and the pdfs).
* ask to commit an empty file first?


-------------------------------------------
**_Scores of Beauty_ Engraving Challenges**
[`<= previous`](4-learning-git.md)
[`main page`](http://github.com/engraving-challenges/main/)
[`next =>`](6-collaboration.md)
