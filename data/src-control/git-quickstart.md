# Git Quickstart

1. Create a repo on the UND-ARC page.
2. Create a folder on your hard drive to act as the local copy.
3. Open a terminal in the folder you just created, and run:

```bash
wget https://github.com/UND-ARC/RepoTemplate/archive/master.zip
unzip -j RepoTemplate-master.zip
rm -rf .git
git init
git remote add origin {URL that's on the front page of the new repo}
git add .
git commit -s -m "Initial Commit" -m "Adding ARC Repository template"
git push origin master
```
