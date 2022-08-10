# Git and Github Tutorial

## Local Git (in Ubuntu/Widows/Mac)

### Commands for local git:

 - To check git version

```bash
git --version
```
 - To configure your name & email

```bash
git config --global user.name "user name of remote git"
git config --global user.email "your email on remote git"
```
 - Another method to add your name & email

```bash
git config --global --edit
```
 - Create a new directory & move into that

```bash
mkdir LetsLearnGit
cd LetsLearnGit
touch Add.java
```
- Initialize local git & check

```bash
git init
ls -al
```
 - Create two inportant files

```bash
touch .gitignore
touch README.md
```
 - check status of files

```bash
git status  # Try to run frequntly 
```
 - Send files from working Directory to Stagging Area

```bash
# To add single file
git add Add.java    
# To add all the files present in current directory
git add .           
```
 - Send files from stagging area to branch

```bash
git commit -m "message of commit"
```
 - To check commit history

```bash
git log     # Try to run frequently
```
#### Shift from one branch to other branch

```bash
# This will delete new changes
git checkout <commit hash code / branch name>
# This will restore newly deleted files
git checkout master/main 
```
 - To check working/current branch

```bash
git branch
```
#### How to create new branch

```bash
git branch test     # Create new branch
git branch          # Check current branch
git checkout test   # Switch to new branch
git branch
```
 - Create new branch & move into that

```bash
git checkout -b vishu/add
touch Add.java
git status
git add Add.java
git commit -m "added Add.java"
git checkout test
```
#### How to merge

```bash
git merge vishu/add
git log
git checkout main/master
git log
git merge test
git log
```

### Remote Git or GitHub

 - For existing repo

```bash
git remote add origin https://github.com/username/reponame.git
git branch -M master/main
git push -u origin master/main
```
### On your terminal

```bash
git remote -v
git remote add origin https://github.com/username/reponame.git
git remote -v
git branch -M master/main
git push -u origin master/main
```
```bash
username: ______________________
password: ______________________
```
 - test branch

```bash
git checkout test
git push -u origin test # Remote repo name "test" and "main"
```