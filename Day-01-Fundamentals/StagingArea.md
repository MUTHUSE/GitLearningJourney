## Staging Area – The Waiting Room

## The staging area (also called index) is where you prepare changes before committing them.



## Three States of Files
Working Directory          Staging Area          Repository
(Your files)               (Index)               (.git commits)

────────────────          ────────────         ──────────────
README.md (modified)
notes.txt (new)
old-file.txt (deleted)

              git add ↓

────────────────          ────────────         ──────────────
                          README.md (staged)
                          notes.txt (staged)
                          old-file.txt (staged)

                                          git commit ↓

────────────────          ────────────         ──────────────
                          (cleared)           README.md (saved)
                                              notes.txt (saved)
                                              old-file.txt (removed)



## Staging Area Commands
# Stage specific file
git add README.md

# Stage all changes
git add .

# View staged changes
git status
# Output:
# On branch main
# Changes to be committed:
#   new file:   README.md
#   modified:   notes.txt

# View difference (staged vs committed)
git diff --staged

# Unstage a file
git reset README.md

# Unstage everything
git reset



## Why Staging Exists?
Scenario: You made 5 changes, but only want to commit 3

Without Staging Area:
git commit          ← Commits ALL 5 changes (can't pick)

With Staging Area:
git add file1.txt   ← Add change 1
git add file2.txt   ← Add change 2
git add file3.txt   ← Add change 3
git commit          ← Commits only 3 changes (others stay as "modified")