## Commits – Snapshots in Time

## A commit is a snapshot of your entire project at a specific moment in time.

Single Commit:
┌─────────────────────────────────┐
│ Commit ID: a1b2c3d4e5f6...      │
├─────────────────────────────────┤
│ Author: Muthu Selvi             │
│ Date: 2026-04-14 10:30:00       │
│ Message: "Day 1: Git Basics"    │
├─────────────────────────────────┤
│ Parent Commit: abc123def...     │
│ Files Snapshot:                 │
│  ├── README.md (content)        │
│  ├── notes.txt (content)        │
│  └── Day-01/ (tree)             │
└─────────────────────────────────┘



## Creating a Commit (3 Steps)
Step 1: Modify Files (Working Directory)
├── Edit file.txt
├── Create new-file.md
└── Delete old-file.txt

Step 2: Stage Changes (Staging Area)
git add .              ← Add all changes

Step 3: Commit (Repository)
git commit -m "message"  ← Save snapshot



## Commit History
# View all commits
git log

# Output:
# commit a1b2c3d4e5f6 (HEAD -> main)
# Author: Muthu Selvi <muthu@email.com>
# Date:   Tue Apr 14 10:30:00 2026 +0530
#
#     Day 1: Git Basics
#
# commit abc123def456
# Author: Muthu Selvi <muthu@email.com>
# Date:   Tue Apr 14 10:00:00 2026 +0530
#
#     Initial commit



## Commit Hash Explained
commit a1b2c3d4e5f6789...

This is a SHA-1 hash:
- Generated from commit content
- Unique identifier for that commit
- Never changes (unless you rewrite history)
- First 7-10 characters usually enough: a1b2c3d