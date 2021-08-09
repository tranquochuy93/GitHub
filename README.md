# GitHub
####
Remote reposity
Local reposity
===========
working tree: directory dang thao tac
-> luu thay doi vao Index
-> Commit => File thay đổi đã lưu ở index được đăng ký vào local repository
-> Push => upload lịch sử thay đổi từ local repository lên remote repository

===============
Pull: download lịch sử thay đổi mời nhất từ remote repository xuống local repository
==== =================
1) Workspace/working tree
2) Staging Area/index
3) Local repository
 
Có 2 trạng thái của file:
Tracked: là tập tin đã được đánh dấu theo dõi trong Git để bạn làm việc với nó.
   + Unmodified: chưa chỉnh sửa
   + Modified: đã chỉnh sửa nhưng chưa đưa vào StagingArea
   + Staged: đã nằm trong StagingArea sẵn sàng commit
Untracked là các tập tin mới được tạo ra và chưa được Git đánh dấu theo dõi.
================
HEAD nó sẽ trỏ đến commit cuối cùng của branch bạn đang thực hiện nằm ở vùng local repository
Nếu có thêm ~ ở cuối nghĩa là commit trước commit cuối cùng.
^ tương đương với ~

xem thông tin commit
git show HEAD

So sánh sự thay đổi giữa

Workingspace - StagingArea: git diff
Workingspace - Local repository: git diff HEAD
StagingArea - Local repository: git diff --cached
---------
- kiểm tra file được thay đổi ở những commit nào
git log faker_harry_potter.txt
- chi tiết hơn
git log -p faker_harry_potter.txt

Như vậy phần StagingArea đã chứa file faker_harry_potter.txt có thay đổi. File faker_harry_potter.txt đang có trạng thái là Tracked và Staged
==================
working directory -> (git add) -> stage/index -> (git commit) -> History
History -> (git reset --soft) -> stage/index
History -> (git reset --mixed) ->working directory 
History -> (git reset --hard) ->xóa thay đổi khỏi stage và working directory
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
### Save change and get it in stash
 ```html
 $ git stash save -u
```
 ```html
 $ git stash pop
```
