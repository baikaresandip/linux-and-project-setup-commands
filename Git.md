# Git 

## Git Commands
### Get the all files changes in the last commit
`git diff --name-only HEAD HEAD~1`
`git log --stat`
`git log -1 --stat --oneline`

### Chery pick
- Make sure you are on the branch where you want to cherry pick
- Run the command `git cherry-pick <commit-hash>`
- 
### Delete branch 
git push -d <remote_name> <branchname>   # Delete remote
git branch -d <branchname>               # Delete local


