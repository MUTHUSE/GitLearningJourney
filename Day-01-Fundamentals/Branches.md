## Branches – Timelines in Git

## A branch is a pointer to a commit. It's like a timeline or a separate line of development.

All Commits (Timeline):
C1 → C2 → C3 → C4 → C5
           ↑
        main (pointer to C4)
        
If you create a new branch:
C1 → C2 → C3 → C4 → C5
     ↓    ↑
     └→ C3a → C3b (feature branch)
           ↑
        feature-x (pointer to C3b)

## Creating Branches
# Check current branch
git branch
# Output:
# * main            ← You're on main (asterisk shows current)

# Create new branch
git branch feature/git-basics
# Creates branch pointing to current commit

# List all branches
git branch -a
# Output:
# * main
#   feature/git-basics
#   remotes/origin/main

# Switch to new branch
git checkout feature/git-basics
git switch feature/git-basics     ← Newer syntax

# Create and switch in one command
git checkout -b Day-01-Concepts
git switch -c Day-01-Concepts     ← Newer syntax

## Branch Points
When you create a branch:
git branch feature-x

Both main and feature-x point to the SAME commit initially

main ─┐
      └→ C4 ← Current commit
feature-x ┘

When you commit on feature-x:
C4 → C4a ← feature-x
↑
main (still pointing to C4)

Now they diverged!