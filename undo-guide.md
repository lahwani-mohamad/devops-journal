# Git Undo Guide

| Situation | Command | Safe after push? (yes/no) |
|---|---|---|
| I want to discard changes in a file that I have not staged. | `git restore file.txt` | Yes |
| I added a file to staging by mistake and want to unstage it. | `git restore --staged file.txt` | Yes |
| I want to correct the message of my last commit. | `git commit --amend -m "New message"` | No |
| I want to safely undo a commit that was already pushed. | `git revert HEAD` | Yes |
| I want to undo the last commit but keep its changes staged. | `git reset --soft HEAD~1` | No |
| I want to undo the last commit and discard its tracked changes. | `git reset --hard HEAD~1` | No |
| I need to save unfinished changes temporarily without committing. | `git stash` | Yes |
