# Theory:
* MongoDB Compass chỉ là môi trường giao diện
* MongoDB Shell dành cho môi trường dòng lệnh
* MongoDB Atlat CLI là môi trường lưu trữ web (cloud)
* Linux ko truy cập đc ứng dụng trên window, Chỉ có window truy cập đc linux, thế nên cài mongodb trên linux vì project có ở linux
* Mongo Shell là một JavaScript interface tương tác với MongoDB, Mongosh là cái tool để viết mongoshell
* khi cài mongoshell về thì mongosh sẽ được kèm theo
* Mongoose là một thư viện JavaScript cho phép bạn định nghĩa các schema với dữ liệu được định kiểu rõ ràng. Khi một schema được định nghĩa, Mongoose cho phép bạn tạo một Model dựa trên một schema cụ thể. Model của Mongoose sau đó được ánh xạ tới một MongoDB document thông qua định nghĩa schema của Model.
*Khi bạn đã xác định các schema và model của mình, Mongoose chứa nhiều hàm khác nhau cho phép bạn xác thực tính hợp lệ, lưu, xóa và truy vấn dữ liệu của bạn bằng các hàm MongoDB phổ biến. Tôi sẽ nói về việc này nhiều hơn với các ví dụ code cụ thể.
* Personal access tokens (PATs) là một giải pháp thay thế cho việc xác thực mật khẩu. Token nó như là 1 password thay thế, tuy nhiên nó có thể phân quyền access khác nhau cho từng token khác nhau và nhiều lựa chọn phân quyền
# Guide GitHub: 
## 1. How To Install GitBash:

- Install this file: [Link GitBash](https://git-scm.com/download/win)

## 2. Open CMD or powershell:

- Config Username: 
   ` git config --global user.name "username Github"`
- Config Gmail: 
   ` git config --global user.email "gmail"`
- Info git 
   ` git config -l `
- Info the project
   ` git remote -v`

## 3. How to create a new repository 

- `git init`

- `git add README.md`

- `git commit -m "first commit"`

- `git branch -M master`

- `git remote add origin git@github.com:name.git`

- `git push -u origin main`

## 4. How to clone a repository 

- `git clone http://github.com/username/filename.git (copy URL)`

## 5. Use stash save

-  `git stash save "add style to our site"`
   
-  `git stash list`
   
-  `git stash show `
   
-  `git stash drop stash@{1}`

-  `git stash clear`

-  `git stash branch add-stylesheet stash@{1}`
   
-  `git stash pop`

## 6. Use favicon

**Readmore:** https://realfavicongenerator.net/faq#.YuorLnbP02w

**Readmore:** Common file validation: https://www.validbot.com/tests.php

**Create an icon combo:**

  1. Go to: https://www.favicon-generator.org/

  2. Choose a file PNG or JPG with size 32x32

  3. Check box with options: Generate icons for Web, Maintain Image Dimensions and Include your favicon.ico in the public gallery
 
  4. Press Create Favicon 

  5. Click on the link "Download the generated favicon" to dowload

**Another link:** https://favicon.io/

**Link test:** https://realfavicongenerator.net/


## 7. Change Github Account 
- `nano ~/.gitconfig`

- `git config -l`

or

- `git config --global user.name "username Github"`
- `git config --global user.email "gmail"`


## 8. Other git
```
git status: kiểm tra trạng thái

git add . : thêm vào Staged

git restore --staged <file or .>: thoát khỏi Staged

git log: xem tất cả commit 

git log --oneline : xem tất cả commit ngắn gọn

git diff: so sánh sự thay đổi giữa file mới chỉnh(chưa add vào Staged) và file commit lần cuối

git diff --staged : so sánh sự thay đổi giữa file Staged (đã add vào Staged) và file commit lần cuối

git diff <IDcommit(1)> <IDcommit(2)>: so sánh sự thay đổi giữa file commit (1) và (2)

git diff <IDcommit(1)> <IDcommit(2)> --stat: so sánh ngắn gọn hơn giữa (1) và (2)

git checkout <mã ID của commit (git log --oneline để lấy mã)> --<file or .>: phục hồi file ở bất kỳ commit nào và file phục hồi sẽ được đánh dấu vào Staged.

git commit --amend -m "<message>": cập nhật file mà ko cần tạo commit (ghi đè lên commit)

-------------------------------------------------------
git reset --soft HEAD~1: xóa commit cuối và đưa về Staged

git reset --hard HEAD~1: xóa commit vĩnh viễn và trả về commit trước đó (nếu số 2 là xóa 2 nhánh liền kề, thêm bao nhiêu thì xóa bao nhiêu)

git reset .: xóa Staged trở về trạng thái khi chưa add

git merge <namebranch>: hợp nhất nhánh main với nhánh <namebranch> đã gọi
git merge --abort: hủy bỏ hợp nhất 2 nhánh khi xung đột

git branch -d <namebranch>:xóa nhánh local

git push origin --delete <namebranch>: xóa nhánh remote

git branch | grep -v 'master' | xargs git branch -D: xóa hết nhánh ở local trừ master 

git log --oneline --graph: xem các nhánh commit với biểu đồ (đỏ: merge lần cuối, xanh: merge từ trước)

git checkout .: nothing to change

git clean -d -f: nothing to change

-----
tạo file .gitignore ở thư mục gốc, sau đó muốn git bỏ qua các file thì soạn cú pháp *.<đuôi tệp> tại file .gitignore

EX:  *.html  *.css   => git sẽ bỏ qua mà không cần duyệt mấy file có đuôi tệp này

EX:  Tep             => git sẽ bỏ qua mà không cần duyệt mấy tệp tin có tên này

# See https://help.github.com/articles/ignoring-files/ for more about ignoring files.
```
## 9. Tạo docker mongo:
```
1. docker pull mongo:latest
2. docker images
3. docker run --name mymongo -d -p 27017:27017 -t mongo:latest
4. docker ps -a
5. docker exec -it mymongo bash
```
## 10. Install mongoshell Ubuntu
1. https://www.mongodb.com/try/download/shell
2. -> MongoDBshell -> DebanUbuntu64-bit (deb)
3. Copylink 
4. Open terminal -> wget https://downloads.mongodb.com/compass/mongodb-mongosh_1.4.2_amd64.deb
5. sudo dpkg -i mongodb-mongosh_1.4.2_amd64.deb
6. check version -> mongosh --version  -> mongosh mongodb://127.0.0.1:27017


## 11. Config SHH keys Github
###### Config SSH Key này trên Github để mỗi lần thực hiện các thao tác với git (clone, commit, push, pull,..) thì Github không yêu cầu nhập mật khẩu nữa. SSH có sẵn trong máy, và là key này dựa vào máy để xác thực
1. Nhấn WIN + I để mở Settings.
2. Mở Apps > Apps & features.
3. Nhấp vào Optional features.
4. Nhấp vào +Add a feature.
5. Duyệt danh sách để tìm OpenSSH Client.
6. Chọn và bấm Install.
7. Terminal github-> ssh-keygen
8. `cat ~/.ssh/id_rsa.pub` or `more id_rsa.pub`
9. github-> setting -> SHHKeys -> New SHH key -> thêm title -> paste all mã id_rsa.pub -> add 

## 12. Recovery reset --hard
#### Case: nếu tất cả các file thay đổi đã được commit
1. Liệt kê history của con trỏ HEAD
```
git reflog

b6eb67c HEAD@{0}: reset: moving to b6eb67c
ff31686 HEAD@{1}: commit: fourth commit
ac79570 HEAD@{2}: reset: moving to HEAD@{1}
b6eb67c HEAD@{3}: reset: moving to b6eb67c
```
2. Rollback về commit
```
git branch <name> ff31686 
```
3. git checkout qua branch đó
```
git checkout <name>
```
#### Case: những thay đổi đã được add nhưng chưa được commit
1. liệt kê các object bị reset hard xóa
```
git fsck --full

Checking object directories: 100% (256/256), done.
dangling blob 9daeafb9864cf43055ae93beb0afd6c7d144bfa4
dangling blob 2894e252ee1a560df965662a8c138b9e16e7dd3b
dangling blob e9e638322fe1703200d5af40e691af0208cf3a97
```
2. tìm id có chứa nội dung bị xóa bởi reset hard
```
git show 3e65ed2670ae277e9d042659dd8639cd0f0f7d9c
HI, my name is ming, and i was deleted by reset hard 
```
3. Copy nội dung này tạo thành file mới để khôi phục lại dữ liệu

## 13. command linux
```
htop: show tiến trình đang chạy
ps -aux: show tiến trình
ps -aux | grep <key-search>: lọc tiến trình theo key-search
ss -l : show các port đang sử dụng
kill <PID> : kill các tiến trình
lsof -i :<port>
```

## 14. docker linux
docker compose là một file shell chứa các command để chạy command đó theo thứ tự
image chứa các container
```
docker ps: show các container đang chạy
docker ps -a: show tất cả container
docker exec -it <name-container> bash: chạy shell trong bash container 
```
## 15. show pdf
```
https://anyflip.com/
```
## 16. api repository
```
https://rapidapi.com/
```
## 17. Finding IP
https://dnsdumpster.com/

https://emojipedia.org/waving-hand/
## 18. Docker Command
```
docker images: Liệt kê các Docker image đang có sẵn trong máy của bạn.
docker ps: liệt kê các Docker container đang chạy.
docker ps -a: liệt kê tất cả container kể các những container đã bị stop.
docker stop <container id/name>: stop một container đang chạy.
docker start <container id/name>: start một container đang bị stop.
docker build -t <image name> .: các bạn lưu ý là có dấu .ở cuối nhé. Ý là kiếm tập tin Dockerfile tại thư mục hiện tại và theo đó tạo thành image tên <image name>.
docker run: chạy image lên và tạo thành container.
docker exec: chạy một lệnh trong môi trường của container đang hoạt động.
docker rm <container>: xoá container.
docker rmi <image>: xoá image.
docker system prune: xoá dữ liệu không sử dụng. Khi bạn bị Docker ăn hết ổ cứng, bạn sẽ cần lệnh này để xoá các container đã bị stop, những image không sử dụng, cache sinh ra trong quá trình tạo image.
```
## 19 Clear cache git
```
git rm -r --cached .
git add .
```


## 99. Query String/Parameters
```
http://www.example.com?search=ruby&results=10
```
<img
  src="https://user-images.githubusercontent.com/59383987/202881114-847acb26-9e27-404e-a55c-cc4371472512.png"
  min-width="400px"
  max-width="400px"
  width="400px"
  alt="PC"
/>
https://viblo.asia/p/tim-hieu-mongodb-phan-2-Zzb7vDEdRjKd
## 100. Template github

<img
  src="https://raw.githubusercontent.com/MicaelliMedeiros/micaellimedeiros/master/image/computer-illustration.png"
  min-width="400px"
  max-width="400px"
  width="400px"
  alt="PC"
/>

<p align="left">
  Hello, i'm Nowbie. Currently working with
  <strong>ReactJS, C# and PHP</strong>. Focused on
  <strong>NodeJS</strong> and <strong>Android development</strong>.<br />
  Right now, i'm studying C# and Android development for
  my projects.
</p>

<p align="left">
  🦄 Skills / Tools:
</p>
<p align="left">
        <a href="https://kotlinlang.org" target="_blank" rel="noreferrer">
    <img
      src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kotlin/kotlin-original.svg"
      alt="Kotlin"
      width="40"
      height="40"
    />
  </a>
  <a href="https://www.java.com" target="_blank" rel="noreferrer">
    <img
      src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg"
      alt="Java"
      width="40"
      height="40"
    />
  </a>
        <a href="https://docs.microsoft.com/pt-BR/dotnet/csharp/tour-of-csharp/" target="_blank" rel="noreferrer">
    <img
      src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg"
      alt="C#"
      width="40"
      height="40"
    />
  </a>
  <a href="https://www.python.org" target="_blank" rel="noreferrer">
    <img
      src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg"
      alt="Python"
      width="40"
      height="40"
    />
  </a>
  <a href="https://www.typescriptlang.org" target="_blank" rel="noreferrer">
    <img
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Typescript_logo_2020.svg/512px-Typescript_logo_2020.svg.png"
      alt="TypeScript"
      width="40"
      height="40"
    />
  </a>
  <a href="https://nodejs.org" target="_blank" rel="noreferrer">
    <img
      src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg"
      alt="Node.js"
      width="65"
      height="40"
    />
  </a>
  <a href="https://reactjs.org" target="_blank" rel="noreferrer">
    <img
      src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg"
      alt="ReactJS"
      width="60"
      height="40"
    />
  </a>
  <a href="https://www.mysql.com" target="_blank" rel="noreferrer">
    <img
      src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-plain-wordmark.svg"
      alt="MySQL / MariaDB"
      width="40"
      height="40"
    />
  </a>
  <a href="https://www.linux.org" target="_blank" rel="noreferrer">
    <img
      src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg"
      alt="Linux"
      width="40"
      height="40"
    />
  </a>
  <a href="https://git-scm.com/" target="_blank" rel="noreferrer">
    <img
      src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg"
      alt="git"
      width="40"
      height="40"
    />
  </a>
  <a href="https://developer.android.com/studio" target="_blank" rel="noreferrer">
    <img
      src="https://upload.wikimedia.org/wikipedia/commons/9/95/Android_Studio_Icon_3.6.svg"
      alt="Android Studio"
      width="40"
      height="40"
    />
  </a>
  <a href="https://insomnia.rest" target="_blank" rel="noreferrer">
    <img
      src="https://icons.iconarchive.com/icons/papirus-team/papirus-apps/96/insomnia-icon.png"
      alt="Insomnia"
      width="40"
      height="40"
    />
  </a>
</p>

<p align="left">
  💌 If you want to carry out a project with me (or make small talk), don't
  hesitate to send me a message: ⤵️
</p>

<p align="left">
  <a href="https://t.me/nowbie" alt="Telegram">
    <img
      src="https://img.shields.io/badge/-Telegram-0e76a8?style=for-the-badge&logo=Telegram&logoColor=white&link=https://t.me/nowbie"
  /></a>
</p>



