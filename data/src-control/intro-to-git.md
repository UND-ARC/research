# Git Introduction

Git is a source version control system.  That means that it controls different
versions of source code.  In a nutshell, Git allows a programmer to change their
workflow from editing one file over and over again until it's "done" to a more
reliable and forgiving workflow of *committing* small changes to a program.
The central unit of Git is a "commit", that is, a discrete change to a file
or files.  Each commit is associated with:

- the "changeset"
- the author of the commit (who made the changes),
- the date and time of the commit,
- a title, summarizing the changes in 80 characters or less (1 line)
- a message (technically optional, but ***highly*** recommended)
  with more details on what was changed, why, etc.

## Branches

A programmer working on a project that lives on their hard drive may wish to
have two slightly different versions of the program.  For example, before
working on a big new feature, they may make a backup of their "master" copy.
This way, ~~if~~when the new feature explodes and destroys the new copy of the
code, the "master" copy remains unharmed.  This can be thought of as a branching
model.  If we represent each change the programmer makes to any of the files
as a commit, we can draw a timeline of each "branch":

```
     |
     |. <-- programmer adds the changes from the "development" copy
     | \    into the "master" copy
     |  | <-- finishes work on the new feature
     |  |
     |  |
     |  | <-- starts work on the new feature
     | /
     |* <-- programmer copies "master" code into separate folder,
     |      begins work on the "development" copy
     |
```

The vertical line to the left represents the master copy of the code as
time progresses.  Time progresses from bottom to top, and we can see at
the asterisk `*` that the programmer creates a second copy.  We call this the
"Development" copy of the code.  In Git, this is referred to as a "branch", and
the act of creating a branch is called "branching."

As the programmer works on the new feature, on the new branch, generally the
master copy remains more or less unchanged.  Note that there is no restriction
on what the branches, or copies, are named -- by convention, the main, working,
ready-to-be-used copy resides in the "master" branch, and most frequently
new features, fixes, etc. are worked on in the "develop" branch.

When the programmer finishes the changes on the develop branch, naturally they
want to apply those changes to the master branch.  This is done with a process
called "merging".  Git can automate most of the actual changes quite easily --
there are situations, however, when manual intervention is needed.  That is a
more complex topic for another guide, but it's important to know that it
happens.  The rundown of merging is that all the changes, or commits, from
one branch (in our case, develop) are applied to (merged) into the main branch
(master).

## Remotes

So far, we have been discussing one programmer working on a program on his/her
computer, entirely outside the reach of any other programmers.  In many cases,
and especially at ARC, we want to collaborate with other programmers.  To do
this, some kind of synchronization method.  The chosen method to do so is a
centralized model.  Programmers upload commits (changes) to GitHub, and other
programmers download them.

### The Difference between Git and GitHub

One of the most commonly mis-explained topics in source control is the
difference between the source control system, Git, and the hub, GitHub.

Git is a version control system.  It keeps track of commits, branches, and a
handful of other small features.

GitHub is a website.  It is where programmers can share their code with each
other all using a version control system (Git).  Git and GitHub are very
tightly integrated, but there is one interesting thing to note:

Git can be used without GitHub, but GitHub cannot be used without Git.

The programmer uses Git to sync their code to and from GitHub, in a manner
that is discussed next.  Importantly, from www.github.com, the programmer
*cannot sync their code*.

### Pushing and Pulling

Because programmers don't trust their computers to make decisions for them,
Git was programmed to sync when it was told to and only then.  Even further,
we have control over whether the direction of the sync:

- A "push" is an 'upward' sync.  It uploads changes from the local environment
  (programmer's hard drive) to the remote (GitHub).
- A "pull" is a 'downward' sync.  It downloads changes from the remote (GitHub)
  to the local environment (programmer's hard drive).

This means that if our coworker, Bob, makes some commits (changes) to the code,
Bob must then "push" his commits to GitHub.  Then, we can "pull" the commits
down to our computer.  We can now run the code, with Bob's changes in it.

The reason for using this centralized model as opposed to having Bob email us
his code is that on a larger scale, as soon as Bob pushes his work to the
server, *anyone* on the team, not just us, can download, test, and further edit
Bob's code.  Once they've edited the code, they repeat the entire process
again.
