# Essential Git Commands & Workflows

> use -h when in doubt like git init -h if u need to know what all things u can do with git init

---

## 📖 Quick Navigation

### Commands

1. [git init](#1-git-init---create-a-new-repository) - Creates a new Git repository on your computer. Used when starting a fresh project from scratch. Git creates a hidden `.git` folder to track all your changes and history.

2. [git clone](#2-git-clone---download-a-project-from-github) - Downloads an entire project from GitHub to your local machine. Used when you want to work on an existing project or contribute to someone else's code. It copies all files, branches, and commit history.

3. [git add](#3-git-add---stage-files-prepare-for-saving) - Prepares files for saving by staging them. Used before every commit to tell Git which changes you want to include. Lets you select specific files or all changes at once.

4. [git commit](#4-git-commit---save-changes-with-a-message) - Saves staged changes as a snapshot with a message. Used after staging to create a permanent record of your work with an explanation of what changed.

5. [git push](#5-git-push---upload-commits-to-github) - Uploads your local commits to GitHub. Used to share your work with teammates and backup your code on the server. Makes your changes visible to others.

6. [git pull](#6-git-pull---download-latest-changes-from-github) - Downloads latest changes from GitHub to your computer. Used to sync with teammates' work before pushing your own changes, preventing conflicts.

7. [git status](#7-git-status---check-what-files-changed) - Shows which files changed, which are staged, and which are untracked. Used anytime to check the current state of your project before staging or committing.

8. [git branch](#8-git-branch---create-and-manage-branches) - Creates and manages separate work areas in your project. Used to work on features or fixes independently without affecting the main code.

9. [git checkout](#9-git-checkout---switch-between-branches) - Switches between branches or reverts file changes. Used to jump between different features you're working on or undo accidental changes.

10. [git merge](#10-git-merge---combine-branches-together) - Combines changes from one branch into another. Used to integrate completed features back into the main project after testing.

11. [git diff](#11-git-diff---see-what-changed) - Shows exactly what changed in files. Used before committing to review your changes and ensure they're correct.

### Tips & Guides
- [Understanding Merge Conflicts](#understanding-merge-conflicts) - Learn how to identify, resolve, and prevent merge conflicts when multiple people edit the same code.

---

## Essential Commands with Parameters

### 1. `git init` - Create a new repository

```
git init                          # Creates .git folder in current directory
git init <folder-name>            # Creates folder and initializes repo
```

**When to use**: Starting a brand new project locally

---

### 2. `git clone` - Download a project from GitHub

```
git clone <URL>                   # Clone entire repo (all branches & history)
git clone <URL> <folder-name>     # Clone into specific folder name
git clone -b <branch-name> <URL>  # Clone specific branch only
```

**When to use**: Getting an existing project to work on locally

---

### 3. `git add` - Stage files (prepare for saving)

```
git add <filename>                # Stage specific file
git add .                         # Stage all changed files
git add *.html                    # Stage all HTML files
git add -A                        # Stage everything (new, modified, deleted)
git add -p                        # Interactive mode - stage parts of files
```

**When to use**: Before committing, to tell Git which files to save

---

### 4. `git commit` - Save changes with a message

```
git commit -m "message"           # Commit with short message
git commit -m "title" -m "description"  # Commit with title and description
git commit --amend                # Modify last commit (add files or fix message)
git commit --amend --no-edit      # Amend without changing message
git commit -h                     # View all options
```

**When to use**: After staging files, to create a snapshot of your code

> **Pro tip**: Write clear messages like "Add login feature" not "fixed stuff"

---

### 5. `git push` - Upload commits to GitHub

```
git push                          # Push current branch to remote
git push origin <branch-name>     # Push specific branch to GitHub
git push -u origin <branch-name>  # Push and set upstream (first time)
git push origin --all             # Push all branches
git push origin --delete <branch> # Delete branch on GitHub
```

**When to use**: After committing locally, to save changes to GitHub

---

### 6. `git pull` - Download latest changes from GitHub

```
git pull                          # Pull from current branch
git pull origin <branch-name>     # Pull specific branch from GitHub
git pull --no-commit              # Fetch without merging automatically
```

**When to use**: Before pushing, to sync latest changes from teammates

---

### 7. `git status` - Check what files changed

```
git status                        # Shows modified, staged, untracked files
git status -s                     # Short format (simpler view)
```

**When to use**: Anytime to see the state of your working directory
**Output guide**:

- Red = modified but not staged
- Green = staged and ready to commit
- Untracked = new files Git doesn't know about

---

### 8. `git branch` - Create and manage branches

```
git branch                        # List all local branches
git branch -a                     # List all branches (local + remote)
git branch <branch-name>          # Create new branch (stays on current)
git branch -d <branch-name>       # Delete branch (safe - prevents data loss)
git branch -D <branch-name>       # Force delete branch
git branch -m <new-name>          # Rename current branch
git branch -h                     # View all options
```

**When to use**: Creating separate work areas for features or fixes

---

### 9. `git checkout` - Switch between branches

```
git checkout <branch-name>        # Switch to existing branch
git checkout -b <branch-name>     # Create AND switch to new branch
git checkout <filename>           # Discard changes in file (revert to last commit)
git checkout HEAD~1               # Go back to previous commit (detached)
git checkout -h                   # View all options
```

**When to use**: Switching between different features you're working on

---

### 10. `git merge` - Combine branches together

```
git merge <branch-name>           # Merge branch into current branch
git merge --no-ff <branch-name>   # Merge with commit (keeps branch history)
git merge --squash <branch-name>  # Combine all commits into one
git merge --abort                 # Cancel merge if conflicts appear
git merge -h                      # View all options
```

**When to use**: After finishing feature, merge back to main
**Important**: Always pull latest before merging to avoid conflicts

---

### 11. `git diff` - See what changed

```
git diff                          # Show unstaged changes
git diff --staged                 # Show staged changes
git diff <branch1> <branch2>      # Compare two branches
git diff <commit1> <commit2>      # Compare two commits
git diff HEAD~1                   # Compare with previous commit
git diff -h                       # View all options
```

**When to use**: Before committing, to review exactly what changed

---

## Understanding Merge Conflicts

> **What is a conflict?** When you and someone else edit the same line and Git doesn't know which version to keep.

**How to resolve:**

```
git merge <branch-name>           # Git will warn about conflicts
# Edit the conflicted files - Git marks them like:
# <<<<<<< HEAD  <-------------------- (conflict markers)
# your changes
# ======= (conflict markers)
# their changes
# >>>>>>> branch-name (conflict markers)

git add <resolved-file>           # Stage the fixed file
git commit -m "Resolve merge conflict"  # Complete the merge
```

**Tips to avoid conflicts:**

- Pull before pushing
- Work on different files when possible
- Communicate with teammates about what you're changing

> Learn more about merge conflicts: https://www.youtube.com/watch?v=DloR0BOGNU0
