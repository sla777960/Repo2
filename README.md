# Git Commands Reference Guide

This guide explains common Git commands and their usage, compiled from our learning sessions.

## Basic Branch Operations

### Creating and Switching Branches
```bash
git branch "branch_name"     # Creates a new branch but stays on current branch
git checkout "branch_name"   # Switches to the specified branch
```
💡 Pro tip: You can combine these commands using `git checkout -b "branch_name"` to create and switch to a new branch in one command.

### Merging Branches
```bash
git merge "branch_name"      # Merges specified branch into current branch (usually main/master)
```
⚠️ Make sure you're on the target branch (e.g., main) before merging!

### Deleting Branches
```bash
git branch -d "branch_name"            # Deletes the branch locally
git push origin --delete "branch_name" # Deletes the branch from remote repository
```
💡 Note: The -d flag will only delete if the branch has been fully merged. Use -D to force delete.

## Remote Repository Operations

### Setting Up Branch Tracking
```bash
git push -u origin branch_name    # Pushes branch and sets up tracking
# or
git push --set-upstream origin branch_name  # Same as above, more verbose syntax
```
This command does two things:
1. Pushes your local branch to the remote repository
2. Sets up tracking between local and remote branches

### Common Workflow Commands
```bash
git add .                         # Stages all changed files
git commit -m "commit message"    # Commits staged changes with a message
git push                         # Pushes commits to remote repository
```

## Best Practices
1. Always create a new branch for new features or fixes
2. Keep commits focused and with clear messages
3. Regularly pull changes from the main branch
4. Delete branches after they're merged to keep repository clean

## Common Gotchas
- Ensure you're in a Git repository before running commands
- Double-check current branch before merging
- Make sure branches are up-to-date before merging
- Use quotes around branch names if they contain spaces

## Additional Tips
- Use `git status` to check current branch and changed files
- Use `git log` to view commit history
- Use `git branch` to list all local branches
- Use `git branch -a` to list both local and remote branches