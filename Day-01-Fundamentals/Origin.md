## Origin – Your Remote Repository Nickname

## Origin is the default name for your remote repository (usually on GitHub).

Your Local Computer          GitHub Server
┌──────────────────┐        ┌────────────────┐
│ GitLearningJ...  │        │ MUTHUSE/Git... │
│ (your machine)   │←origin→│ (github.com)   │
│ git init done    │        │ Remote copy    │
└──────────────────┘        └────────────────┘



## Setting Up Origin
# When you clone, origin is set automatically
git clone https://github.com/MUTHUSE/GitLearningJourney.git

# View your remotes
git remote -v
# Output:
# origin  https://github.com/MUTHUSE/GitLearningJourney.git (fetch)
# origin  https://github.com/MUTHUSE/GitLearningJourney.git (push)

# If creating repo locally, add origin manually
git remote add origin https://github.com/MUTHUSE/GitLearningJourney.git



## Pushing to Origin
# Push your commits to GitHub
git push origin main

# Push a specific branch
git push origin feature/new-login

# Set origin as upstream (default for future pushes)
git push -u origin main



## Fetching from Origin
# Download changes from GitHub (without merging)
git fetch origin

# Download and merge
git pull origin main