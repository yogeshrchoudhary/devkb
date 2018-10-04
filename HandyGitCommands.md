# Handy Git commands
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
