# Guide GitHub: 
## 1. How To Install GitBash:

- Install this file: [Link GitBash](https://git-scm.com/download/win)

## 2. Open CMD or powershell:

- Config Username: 
   ` git config --global user.name "username Github"`
- Config Gmail: 
   ` git config --global user.email "gmail"`
  
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



## 8. demo
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


## 9. Template github

<img
  src="https://raw.githubusercontent.com/MicaelliMedeiros/micaellimedeiros/master/image/computer-illustration.png"
  min-width="400px"
  max-width="400px"
  width="400px"
  align="right"
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




