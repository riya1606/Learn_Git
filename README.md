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

## 3. Git Branching
## 4. Git Teamwork
