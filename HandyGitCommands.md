
# Personal Git Tips
## Handy Git commands
* To find the remote repository for a local one
  ```
  git config --get remote.origin.url
  ```
* To remove a remote repository from a local one
```
git remote remove origin
```
* Push an existing repository from local
```
git remote add origin <remote-repository-url>
git push -u origin --all
```
* Switch remote URL
```
git remote set-url origin https://MyTasks4PE@dev.azure.com/MyTasks4PE/PEDashboard/_git/IonicConference
```
* Verify remote URL
```
git remote -v
```
* Merge changes from remote repository to local repository
  ```
  git pull
  ```

* Remove a file from the local repository
   ```
  git rm 'filename'
  ```

* Commit changes to the local repository
   ```
   git commit
   ```
   
* Push the local repository commits to remote repository
  ```
  git push origin master
  ```
* Shelving your work
  * To move your temporary code to repository use,
  ```
  git stash
  ```
  To move your temporary code to repository and provide a friendly name to retrieve it back, use,
  ```
  git stash save "stash name"
  ```
  * Display list of modifications done
  ```
  git stash list
  ```
  This displays all stashes along with the indexes where they were stashed.
  * Display what modifications were done in the last stash
  ```
  git stash show
  ```
  * Display what modifications were done in a specific stash
  ```
  git stash show -p stash@{stash-number}
  ```
  * To pull back you last temporary code from repository (i.e. TFS unshelve)
  ```
  git stash pop
  ```
  To pull back code stashed away at a specific stash index use
  ```
  git stash pop stash@N
  ```
  This will remove the stashed code at index N.
  To pull back code stashed away at a specific stash index, but still keep the stashed code in the repo, use
  ```
  git stash apply stash@N
  ```
### Branching
  * Create a branch in the local repo
  ```
  git branch 'branch-name'
  ```
  * Display list of branches
  ```
  git branch [-r] [-v] [--sort=[-]committerdate]
  ```
  Without any options _git branch_ will display list of local branches. _-r_ displays remote branches. _-v_ displays branches sorted on latest commits. _--sort=committerdate_ displays in the ASC order of commits. To display in the DESC order of commits use _-committerdate_.
  * Delete a branch
  To delete a branch on the remote use
  ```
  git push --delete 'remote name' 'branch name'
  ```
  Note _remote name_ would mostly be _origin_.
  To delete a branch locally, use
  ```
  git branch -d 'branch name'
  ```
  * Push a branch to the remote even if no changes are made to the local repo
  ```
  git push -u origin 'branch-name'
  ```
  * Merge a different branch to current branch
  ```
  git merge 'branch-name'
  ```
  * Compare 2 branches
  ```
  git diff branch1..branch2
  ``` 
   Compare same file in 2 branches
  ```
  git diff branch1..branch2 'filename'
  ```
  To understand the format of _diff_ output see the StackOverflow link [here](https://stackoverflow.com/questions/2529441/how-to-read-the-output-from-git-diff).
   
   Compare which files have changes in 2 branches
  ```
  git diff --name-status branch1..branch2
  ```
  Renaming a branch, See [here](https://linuxize.com/post/how-to-rename-local-and-remote-git-branch/)
  
### Few more commands
  Checkout all files from a specific commit
  ```
  git clone <repo-url>
  git checkout <commit-sha>
  ```
  
* Undoing changes
  * Undo all changes locally
  ```
  git reset --hard
  ```
  * Undo changes to a specific file locally i.e. set it back to the HEAD at the remote
  ```
  git checkout @ --'filename'
  ```
* View history of commits
  ```
  git log
  ```
  This should give the detailed history along with the author, datetime of the commit.
  To view the shorter history version use,
  ```
  git log --oneline
  ```
* View branch tree
  ```
  git log --graph --oneline --all
  ```

## Useful references
1. [Git Labs documentation](https://git-scm.com/docs)
2. [Git Command used everyday](https://git-scm.com/docs/giteveryday)
3. [Naming Git branches](https://stackoverflow.com/questions/273695/git-branch-naming-best-practices)
4. [Azure DevOps Git](https://docs.microsoft.com/en-us/azure/devops/repos/git/?view=vsts)
