---
title: Important Git Commands I've Learned
published: 2025-03-13
description: 'Good to know basic git commands for you to use in coding'
tags: ["ZeroToDev", "Git"]
category: DevNotes
draft: false 
lang: ''
---

# All Git Commands i've learned so far

## Git Commands are important.
In my opinion, to contribute a lot of code either for your own project or for someone else's project, you really need to know how to use git commands. So this is the reason why i made this page to remind myself every git commands i've learned so far. If i learned something new about git commands, i will update this page.


### 1. **git config**

When you first install git, it's important to setup and configure your git so it understands who you are when working with git. You can do this by going to your terminal and run this command:

```
format:
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"

```

usage example:
```
git config --global user.name "jane_doe"

```

```
git config --global user.email "jane_doe@example.com"

```

This will allow git to associate work you do with your account.

to see all the configuration list, you can run this command:

```
git config --list

```

### 2. **git init**

This command is used to create an empty git repository or reinitialize an existing one.

first, move inside your project folder/open visual code inside your project folder

cd name-of-your-project / use ui to open visual code inside your project folder

then run this command:

```

git init

```

this command will create hidden folder called .git inside your project folder and it will save all your important data to track changes in your project.

### 3. **git status**

This command is used to check the status of your git repository.

```

git status

```

if there is some untracked files, git will show you the list of files that are not being tracked by git.

### 4. **git add**

There are few ways to use git commands.

- git add .

We can use git add . to add all files to the staging area from working directory to staging area.

- git add filename
We can also use git add filename to ad a specific file to the staging area

example of usage:

```
Let's say you make few changes to a lot of files or you create new files

you go to terminal and run:

git add .

this will add all the files to the staging area (that is not being tracked by git)

```

```
Next one you just made simple changes or maybe fix small problems which doesn't require you to add all the files to the staging area

then you use this command in terminal:

git add userModel.js

this will add userModel.js to the staging area

```

> Think of git add as telling git "okay please keep track of this file in its current state". if you make changes to the file, then you need to use git add again to keep track of those newer changes.

### 5. **git commit**

this command is used to savve the changes you made inside your project folder into the repository git with a short message that describes what you did.

```

git commit -m "your commit message"

```

example of usage:

```

git commit -m "Add new function to userModel.js"

```

### 6. **git clone**

This command will be used when you want to clone a project folder that you need to make changes to.

The steps are as follows:

a. Go to the github page of the project you want to clone
b. Click on the green button that says "Code"
c. Select the option that says "HTTPS"
d. Click the copy icon to copy the url
e. Go to your terminal and run this command:

```

git clone url-that-you-copied

```

example of usage:

```

git clone https://github.com/username/project-name.git

```

f. Press enter and once you see done, now you have the project folder in your computer.

### 7. **git branch**

it is important to add changes to a new branch instead of the main branch. A branch in git repository is like a separate version of a document so you didn't mess up with the original.

to create new branch, you can use this command:

```

git checkout -b branch-name

```

this will create new branch and switch to that branch.

To see the list of the branches that you have, you can use this command:

```

git branch

or

git branch --list

```

to switch to a different branch, you can use this command:

```

git switch branch-name

or

git checkout branch-name

```

to delete a branch, you can use this command:

```
this will delete branch locally

git branch -d branch-name

```

```
this will delete branch remotely (in repository)

git push -delete origin branch-name

```

### 8. **git push**

This command tells git thanks for tracking these file changes, now i want to upload these changes to the main project file. You are essentially pushing your changes to the main project file.

```

git push remote branch-name

```

example of usage:

```

git push origin feat/add-new-function

```

once you push your changes, you can go to github and see there is a new branch available to merge.

### 9. **git pull**

Lets say your team merge the update the main branch with the changes you have made while also they made some changes and merge it to the main branch. That means you need to update your local repository with the changes that they have made so it will be up to date with the main branch that your team is working on. You can do this by using this command:

```

git pull remote branch-name

```

pull from the branch that your team already merged, lets say the branch that your team using is develop as a branch to merge from other branch like feat/add-new-function

that means you will use this command:

```

git pull origin develop

```


### Proper Github Flow

(need to update this github flow)

- git clone

- git checkout -b branch-name

- git add .

- git commit -m "your commit message"

- git push origin branch-name

- open pull request

- merge pull request and delete branch


Learning resources:

- https://git-scm.com/docs
- https://github.blog/developer-skills/github/top-12-git-commands-every-developer-must-know/
- https://www.freecodecamp.org/news/10-important-git-commands-that-every-developer-should-know/