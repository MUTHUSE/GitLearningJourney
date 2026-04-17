Git (Version Control Tool)
    ↓
Directory (Folder) + git init
    ↓
Repository (.git folder created)
    ↓
Commits (Snapshots)
    ↓
Branches (Timelines)
    ↓
Remotes (GitHub/origin)



| Concept       | What It Is               | Command	          | Purpose                |
| Git	        | Version control system   | git --version	      | Track code changes     |
| Directory	    | Regular folder	       | mkdir folder	      | Contains files         |
| Repository    | Directory + .git	       | git init	          | Enable version control |
| .git	        | Hidden metadata folder   | ls -la	              | Stores all history     |
| Branch	    | Line of development	   | git branch	          | Separate work streams  |
| Main	        | Primary branch	       | git checkout main	  | Production code        |
| Origin	    | Remote repo nickname	   | git remote -v	      | GitHub location        |
| Commit	    | Snapshot in time	       | git commit -m "msg"  | Save work              |
| Staging Area	| Pre-commit buffer	       | git add .	          | Prepare changes        |
| Working Dir	| Your actual files	       | ls -la	              | Current state          |

## Key Takeaways from Day 1
Git = Tool for tracking code changes over time
Directory = Regular folder with files
Repository = Directory with .git/ folder (Git-enabled)
Commits = Snapshots of your project
Branches = Separate timelines of commits
Main = Primary/default branch
Origin = Remote repository (on GitHub)
Staging Area = Pre-commit preparation area