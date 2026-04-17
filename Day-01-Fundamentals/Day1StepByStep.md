# ============================================
# STEP 1: Create a Directory
# ============================================
mkdir GitLearningJourney
cd GitLearningJourney
pwd                    # Verify location

# ============================================
# STEP 2: Initialize Repository
# ============================================
git init

# Output:
# Initialized empty Git repository in /path/to/GitLearningJourney/.git/

# Verify .git folder exists
ls -la
# drwxr-xr-x  .git

# ============================================
# STEP 3: Check Status
# ============================================
git status

# Output:
# On branch main
# No commits yet
# nothing to commit

# ============================================
# STEP 4: Create Files
# ============================================
echo "# Git Learning Journey" > README.md
echo "Day 1 - Understanding Fundamentals" > notes.txt

git status
# Output:
# Untracked files:
#   README.md
#   notes.txt

# ============================================
# STEP 5: Stage Files
# ============================================
git add .

git status
# Output:
# Changes to be committed:
#   new file:   README.md
#   new file:   notes.txt

# ============================================
# STEP 6: Create First Commit
# ============================================
git config user.email "your@email.com"      # One-time setup
git config user.name "Your Name"            # One-time setup

git commit -m "Initial commit: Day 1 Git Basics"

# Output:
# [main (root-commit) a1b2c3d] Initial commit: Day 1 Git Basics
#  2 files changed, 2 insertions(+)
#  create mode 100644 README.md
#  create mode 100644 notes.txt

# ============================================
# STEP 7: View Commit History
# ============================================
git log

# Output:
# commit a1b2c3d4e5f6 (HEAD -> main)
# Author: Your Name <your@email.com>
# Date:   Tue Apr 14 10:30:00 2026 +0530
#
#     Initial commit: Day 1 Git Basics

# ============================================
# STEP 8: Create Branch & Switch
# ============================================
git checkout -b Day-01-Concepts

# ============================================
# STEP 9: Make Changes on New Branch
# ============================================
mkdir Day-01-Git-Basics
echo "Repository = Directory + .git" > Day-01-Git-Basics/concepts.txt

git add Day-01-Git-Basics/
git commit -m "Day 1: Add Git concepts notes"

# ============================================
# STEP 10: View Branches
# ============================================
git branch
# Output:
#   main
# * Day-01-Concepts

# ============================================
# STEP 11: Switch Back to Main
# ============================================
git checkout main

# ============================================
# STEP 12: Merge Branch to Main
# ============================================
git merge Day-01-Concepts

# Output:
# Updating a1b2c3d..e5f6g7h
# Fast-forward
#  Day-01-Git-Basics/concepts.txt | 1 +
#  1 file changed, 1 insertion(+)

# ============================================
# STEP 13: View Final History
# ============================================
git log --oneline --graph

# Output:
# * e5f6g7h (HEAD -> main, Day-01-Concepts) Day 1: Add Git concepts notes
# * a1b2c3d Initial commit: Day 1 Git Basics