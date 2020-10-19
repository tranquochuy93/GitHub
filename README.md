# GitHub

#### Create new brand
1) create new brand at local from other branch
  - create new brand from origin
    ```html
    $ git checkout -b myFeature orgin
    ```
  - create new brand from origin/feature/111 branch
    ```html
    $ git checkout -b myFeature origin/feature/111
    ```
2) push myFeature branch to remote at origin
    ```html
    $ git push origin myFeature
    ```
#### Commit and push
1) pull source code to check conflic
   ```html
    $ git pull
   ```
2) add file, revert, remove file to commit
3) commit
  ```html
   $ git commit -m "message" -n
  ```
4) push
  ```html
   $ git push
  ```
