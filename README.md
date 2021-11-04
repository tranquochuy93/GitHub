# Ubuntu
### Clone git using private ssh key
```bash
Keys need to be only readable by you
chmod 400 ~/.ssh/id_rsa

If Keys need to be read-writable by you
chmod 600 ~/.ssh/id_rsa
```
```bash
ssh-agent bash -c 'ssh-add ~/.ssh/id_rsa_hodfords; git clone git@gitlab.com:diginexhk/lumen/lumen-backend.git'
```

### Install MS font
```cmd
wget http://ftp.de.debian.org/debian/pool/contrib/m/msttcorefonts/ttf-mscorefonts-installer_3.6_all.deb

sudo dpkg -i ttf-mscorefonts-installer_3.6_all.de
```

### Install Arial unicode font
```cmd
1) sudo mkdir /usr/share/fonts/truetype/arialuni/

2) tar -jxvf arial.tar.bz2 arialuni/arialuni.ttf

3) sudo cp arialuni/arialuni.ttf /usr/share/fonts/truetype/arialuni/

4) sudo chmod 644 /usr/share/fonts/truetype/arialuni/arialuni.ttf

5) rm -r arialuni/

6) sudo fc-cache -f -v
```
# GitHub
### push project to repository
1. create repository "microservice-kafka"
2. create local project
3. run cmd
```cmd
git init
git add .
git commit -m "create-project"
git remote add origin https://github.com/tranquochuy93/microservice-kafka.git
git push -u origin master
```
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
