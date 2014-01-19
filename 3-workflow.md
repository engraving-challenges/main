#### openLilyLib Engraving Challenges

# General Challenge Rules / Contributor's Guide

If you participate in an **openLilyLib Engraving Challenge** you should
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

Each challenge resides in its own repository in our [Github organization]

For each participating program (or participant) there will be a dedicated
directory. Inside this directory you can do what you want, adding subdirectories
for any tools, include or intermediate files or whatever.
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

---

Back to the [main page](README.md)
