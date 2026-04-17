## Repository – Directory + Git Magic

## A repository is a directory that has been initialized with Git using git init.

Transformation: Directory → Repository

BEFORE (Regular Directory)
📁 GitLearningJourney/
├── 📄 README.md
└── 📄 notes.txt

↓ git init ↓

AFTER (Git Repository)
📁 GitLearningJourney/
├── 📁 .git/              ← NEW! Hidden folder
│   ├── objects/
│   ├── refs/
│   ├── HEAD
│   ├── config
│   └── ...
├── 📄 README.md
└── 📄 notes.txt

## Creating a Repository
# Method 1: Initialize empty directory
mkdir MyProject
cd MyProject
git init

# Method 2: Clone existing repository
git clone https://github.com/MUTHUSE/GitLearningJourney.git
cd GitLearningJourney

## What Makes It a Repository?
The .git/ folder! This hidden folder contains:
✅ All commits (history)
✅ Branches information
✅ Configuration settings
✅ Remote information (GitHub link)
✅ Everything Git needs to track changes