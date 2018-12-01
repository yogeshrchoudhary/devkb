# Personal Git knowledge base
## Handy Git commands
* To find the remote repository for a local one
  ```
  git config --get remote.origin.url
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
  * Display list of modifications done
  ```
  git stash list
  ```
  * Display what modifications were done in the last stash
  ```
  git stash show
  ```
  * To pull back you temporary code from repository (i.e. TFS unshelve)
  ```
  git stash pop
  ```
* Branching
  * Create a branch in the local repo
  ```
  git branch 'branch-name'
  ```
  * Display list of branches
  ```
  git branch [-r] [-v] [--sort=[-]committerdate]
  ```
  Without any options _git branch_ will display list of local branches. _-r_ displays remote branches. _-v_ displays branches sorted on latest commits. _--sort=committerdate_ displays in the ASC order of commits. To display in the DESC order of commits use _-committerdate_.
 * Push a branch to the remote even if no changes are made to the local repo
  ```
  git push -u origin 'branch-name'
  ```
 * Merge a different branch to current branch
  ```
  git merge 'remote-branch-name'
  ```
 * Compare 2 branches
  ```
  git diff branch1..branch2
  ```
  Compare same file in 2 branches
  ```
  git diff branch1..branch2 'filename'
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

## Useful references
1. [Git Labs documentation](https://git-scm.com/docs)
2. [Git Command used everyday](https://git-scm.com/docs/giteveryday)
3. [Naming Git branches](https://stackoverflow.com/questions/273695/git-branch-naming-best-practices)
4. [Azure DevOps Git](https://docs.microsoft.com/en-us/azure/devops/repos/git/?view=vsts)
