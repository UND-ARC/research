# Git Commands

See [this file](intro-to-git.md) for an introduction to the principles that
precede the functions detailed in this document.

## Enabling Git for a directory

From your existing code directory, open a terminal, and enter:

```
git init
```

Done!

## Adding files to the stage

At first, Git does not track your files.  To "add" a file to the "stage", that
is, the list of files to be committed, do:

```
git add {filename}
```

For example, to add, or stage, an edited file `Hello.world`, one could run any
of the following:

```
git add Hello.world  # add only this file
git add *.world      # add any file with the .world extension
git add Hello.*      # add any file starting with "Hello."
git add .            # add everything
```

## Committing changes

Once files have been staged, the next step is to commit the changes.  The
commit command has a few extra arguments, briefly summarized here:

```
git commit -s -m "Commit title" -m "More details about the changes contained"

-s           : Sign off commits.  Adds "Author Name <author.email@example.com>"
               to the commit message.  Committing will work fine without, but
               required at ARC.
-m <message> : Each time -m <message> is added, a new paragraph is added to
               the commit message.  The first one is the title, which should
               always be less than 80 characters.
```

## Pushing changes to a remote

To be able to push to a remote, you must first add a "remote tracker" to the
local Git data.  To do this, run:

```
git remote add origin <GitHub repo URL ending in ".git">
```

Then, to push, run:

```
git push origin <branch>
```

where `<branch>` is the branch you're currently editing.  ***YOU SHOULD NEVER
PUSH TO MASTER***.

## Pulling changes from a remote

To pull changes from a remote, run:

```
git pull
```

and Git will pull from the remote branch mirroring your current local branch.
