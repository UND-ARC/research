**[Back to Source Control](https://und-arc.github.io/research/src-control/index.html)**

# Git Quickstart

## Creating a new repository

1. Create a repo on the UND-ARC page.
2. Create a folder on your hard drive to act as the local copy.
3. Open a terminal in the folder you just created, and run:

```bash
wget https://github.com/UND-ARC/RepoTemplate/archive/master.zip
unzip -j RepoTemplate-master.zip
rm -rf .git
git init
git remote add origin {URL from the front page of the new repo}
git add .
git commit -s -m "Initial Commit" -m "Adding ARC Repository template"
git push origin master
```

## Adding a preexisting repository (from remote)

1. Create a folder on your hard drive to act as the local copy.
2. Open a terminal in the folder you just created, and run:

```bash
git clone {URL for the existing repo page}
```
