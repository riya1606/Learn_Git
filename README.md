# Learn_Git
Learn to save and manage different versions of your code projects with this essential tool.
## 1. Basic Git Workflow
### A. Hello Git
Git is a software that allows you to keep track of changes made to a project over time. Git works by recording the changes you make to a project, storing those changes, then allowing you to reference them as needed.
### B. Git init

```
git init
```
The word init means initialize. The command sets up all the tools Git needs to begin tracking changes made to the project.
### C. Git Workflow
![Git Workflow](https://user-images.githubusercontent.com/62128029/134795695-755b0078-1b9e-4c12-9887-7cdabb864d28.png)

Nice! We have a Git project. A Git project can be thought of as having three parts:

* A Working Directory: where you’ll be doing all the work: creating, editing, deleting and organizing files
* A Staging Area: where you’ll list changes you make to the working directory
* A Repository: where Git permanently stores those changes as different versions of the project.
The Git workflow consists of editing files in the working directory, adding files to the staging area, and saving changes to a Git repository. 

### D. Git Status
```
git status
```
The git status command displays the state of the working directory and the staging area.
### E. Git Add
```
git add filename
```
The git add command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit.
### F. Git Diff
```
git diff filename
```
git diff is a multi-use Git command that when executed runs a diff function on Git data sources. These data sources can be commits, branches, files and more. The git diff command is often used along with git status and git log to analyze the current state of a Git repo.
### G. Git Commit
```
  git commit -m "message"
```
A commit is the last step in our Git workflow. A commit permanently stores changes from the staging area inside the repository.One more bit of code is needed for a commit: the option -m followed by a message.
### H. Git Log
```
git log
```
Often with Git, you’ll need to refer back to an earlier version of a project. Commits are stored chronologically in the repository and can be viewed with git log
## 2. How to Backtrack in Git
When working on a Git project, sometimes we make changes that we want to get rid of. Git offers a few eraser-like features that allow us to undo mistakes during project creation.
### A. Head Commit
In Git, the commit you are currently on is known as the HEAD commit. In many cases, the most recently made commit is the HEAD commit.
```
git show HEAD
```
The output of this command will display everything the git log command displays for the HEAD commit, plus all the file changes that were committed.

### B. Git Checkout
```
git checkout HEAD filename
```
The command will restore the file in your working directory to look exactly as it did when you last made a commit.

### C. More Git Add
In Git, it’s common to change many files, add those files to the staging area, and commit them to a repository in a single commit.
```
git add file_name1 filename_2
```
This way you can add multiple files to the staging area.

### D. Git Reset
This command resets the file in the staging area to be the same as the HEAD commit. It does not discard file changes from the working directory, it just removes them from the staging area.
```
git reset HEAD filename
```
To hard reset files to HEAD on Git, use the “git reset” command with the “–hard” option and specify the HEAD. The purpose of the “git reset” command is to move the current HEAD to the commit specified.
```
git reset commit_SHA
```
You just need to specify first 7 characters of the SHA of a previous commit.
For Example:
```
git reset 5d69206
```
## 3. Git Branching
Up to this point, you’ve worked in a single Git branch called master. Git allows us to create branches to experiment with versions of a project. Imagine you want to create version of a story with a happy ending. You can create a new branch and make the happy ending changes to that branch only. It will have no effect on the master branch until you’re ready to merge the happy ending to the master branch.
Once you switch branches, you will now be able to make commits on the branch that have no impact on master.
### A. Current Branch
To check which branch you are currently on.
```
git branch
```
In the output, the * (asterisk) is showing you what branch you’re on.
### B. Branching Overview
![Branching Github](https://user-images.githubusercontent.com/62128029/134799097-9638ea66-9c8f-4748-88c0-490d1ef419b4.png)
To create a new branch:
```
git branch new_branch
```
### C. Git Checkout
You can switch to the new branch with:
```
git checkout branch_name
```
### D. Commit on a New Branch
To add files to the staging area:
```
git add filename
```
To commit
```
git commit -m "Commit message"
```
### E. Git Merge
The git merge command lets you take the independent lines of development created by git branch and integrate them into a single branch.
```
git merge branch_name
```
To switch branches: A quick way of switching branch on Git is to use the “git checkout” command and specify the name of the branch you want to switch to.
```
git checkout master
```
### F. Delete Branch
In Git, branches are usually a means to an end. You create them to work on a new project feature, but the end goal is to merge that feature into the master branch. After the branch has been integrated into master, it has served its purpose and can be deleted.
The following command will help to do so:
```
git branch -d branch_name
```

## 4. Git Teamwork
