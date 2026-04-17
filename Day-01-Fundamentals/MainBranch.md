## Main Branch – Your Primary Timeline
What is Main?
Main (formerly master) is the default branch in modern Git repositories.

Repository Branches:
├── main (Production-ready code)
│   ├── Stable version
│   ├── Merged from other branches
│   └── Usually protected from direct commits
│
├── develop (Development version)
│   └── Testing ground
│
├── feature/login (Temporary branch)
│   └── Work on new feature
│
└── bugfix/issue-123 (Temporary branch)
    └── Fix a specific bug

## Why Main Matters
Development Workflow:
1. Start on main (stable code)
   git checkout main

2. Create feature branch
   git checkout -b feature/new-login

3. Work and commit on feature branch
   (main stays clean)

4. Merge feature back to main
   git checkout main
   git merge feature/new-login

5. Now main has new feature + stays stable