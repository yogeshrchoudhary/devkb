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
* Similar to TFS shelve
  ```
  git stash
  ```
* Similar to TFS unshelve
  ```
  git stash pop
  ```
* Create a branch in the local repo
  ```
  git branch 'branch-name'
  ```
* Push a branch to the remote even if no changes are made to the local repo
  ```
  git push -u origin 'branch-name'
  ```
* Undo all changes locally
  ```
  git reset --hard
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

## Useful references
1. [Git Labs documentation](https://git-scm.com/docs)
2. [Git Command used everyday](https://git-scm.com/docs/giteveryday)
3. [Naming Git branches](https://stackoverflow.com/questions/273695/git-branch-naming-best-practices)
4. [Azure DevOps Git](https://docs.microsoft.com/en-us/azure/devops/repos/git/?view=vsts)
