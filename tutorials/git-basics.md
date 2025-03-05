# Git Commands Reference Guide

## Basic Git Configuration
```bash
# Set up your name and email
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check current configuration
git config --list
```

## Repository Initialization
```bash
# Create a new repository
git init

# Clone an existing repository
git clone <repository-url>
```

## Working with Branches
```bash
# List all local branches
git branch

# List all branches (local and remote)
git branch -a

# Create a new branch
git branch <branch-name>

# Switch to a branch
git checkout <branch-name>

# Create and switch to a new branch in one command
git checkout -b <new-branch-name>

# Rename a branch
git branch -m <old-branch-name> <new-branch-name>

# Delete a branch
git branch -d <branch-name>

# Force delete a branch (even if not merged)
git branch -D <branch-name>
```

## Staging and Committing
```bash
# Check status of working directory
git status

# Add specific file to staging area
git add <filename>

# Add all changed files to staging area
git add .

# Commit staged changes
git commit -m "Commit message"

# Commit all modified tracked files
git commit -am "Commit message"

# Amend the most recent commit
git commit --amend
```

## Merging and Rebasing
```bash
# Merge a branch into current branch
git merge <branch-name>

# Rebase current branch onto another branch
git rebase <branch-name>

# Interactive rebase
git rebase -i HEAD~3
```

## Remote Repositories
```bash
# Add a remote repository
git remote add origin <repository-url>

# List remote repositories
git remote -v

# Push changes to remote repository
git push origin <branch-name>

# Pull changes from remote repository
git pull origin <branch-name>

# Fetch changes without merging
git fetch origin
```

## Checking History and Differences
```bash
# View commit history
git log

# View compact commit history
git log --oneline

# Show changes between commits
git diff <commit1> <commit2>

# Show changes in staging area
git diff --staged

# View commit details
git show <commit-hash>
```

## Undoing Changes
```bash
# Unstage a file
git reset <filename>

# Discard local changes in working directory
git checkout -- <filename>

# Revert a commit (creates a new commit that undoes changes)
git revert <commit-hash>

# Reset to a previous commit (be careful!)
git reset --hard <commit-hash>
```

## Stashing Changes
```bash
# Stash current changes
git stash

# List stashed changes
git stash list

# Apply most recent stash
git stash apply

# Apply and remove most recent stash
git stash pop

# Create a named stash
git stash save "Description of stash"
```

## Advanced Operations
```bash
# Cherry-pick a commit from another branch
git cherry-pick <commit-hash>

# Create and apply a patch
git format-patch <branch-name>
git am <patch-file>
```

## Useful Git Aliases
```bash
# Example aliases to add to ~/.gitconfig
[alias]
    co = checkout
    br = branch
    ci = commit
    st = status
    lg = log --oneline --graph --decorate
```

## Best Practices
- Commit often
- Write clear, descriptive commit messages
- Use branches for new features or experiments
- Pull and merge remote changes regularly
- Use .gitignore to exclude unnecessary files
