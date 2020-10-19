# GitHub

### Create new brand
1) create new brand at local from other branch
  - create new brand from origin
    ```html
    $ git checkout -b feature/issues/222 origin
    ```
  - create new brand from origin/feature/issues/111 branch
    ```html
    $ git checkout -b feature/issues/222 origin/feature/issues/111
    ```
2) push feature/issues/222 branch to remote at origin
    ```html
    $ git push origin feature/issues/222
    ```
### Commit and push
1) pull source code to check conflic
   ```html
    $ git pull
   ```
2) add file, revert, remove file to commit
  - show current branch and modified files
   ```html
    $ git status 
   ```
  - add file to commit
   ```html
    $ git add foo/bar/file.vue 
   ```
3) commit
    ```html
     $ git commit -m "message" -n
    ```
4) push
  ```html
   $ git push origin feature/issues/222
  ```
