# Guide GitHub: 
## 0. Git Advance
```
git stash: Lưu những thay đổi chưa được commit và đưa chúng vào stash stack.
git cherry-pick: Chọn một commit cụ thể và áp dụng nó vào branch hiện tại.
git rebase: Chuyển đổi lịch sử commit của branch hiện tại bằng cách áp dụng các commit của branch khác lên branch hiện tại.
git reflog: Liệt kê tất cả các hoạt động của git đã được thực hiện trên repository, kể cả khi các commit đã bị xoá hoặc reset.
git bisect: Tìm kiếm một commit đã gây ra lỗi bằng cách kiểm tra từng commit một.
git submodule: Thêm các repository con như một phần của repository chính.
git filter-branch: Lọc lại lịch sử commit của repository.
git revert: Tạo ra một commit mới để khôi phục lại trạng thái của repository tại một commit trước đó.
git blame: Tìm kiếm các thông tin về lịch sử commit của một file cụ thể.
git tag: Gắn nhãn cho một commit cụ thể để đánh dấu một phiên bản hoặc một trạng thái của repository.

git bisect start: Bắt đầu quá trình tìm kiếm lỗi với git bisect.
git bisect good: Đánh dấu một commit là đúng trong quá trình tìm kiếm lỗi với git bisect.
git bisect bad: Đánh dấu một commit là sai trong quá trình tìm kiếm lỗi với git bisect.
git bisect reset: Kết thúc quá trình tìm kiếm lỗi với git bisect và quay trở lại trạng thái ban đầu.
git cherry: Chọn một số commit cụ thể và áp dụng chúng vào branch hiện tại.
git clean: Xoá các tệp tin chưa được theo dõi bởi Git.
git config: Cấu hình các tùy chọn cho Git.
git diff: So sánh các thay đổi giữa các phiên bản của repository.
git log: Hiển thị lịch sử commit của repository.
git merge: Hợp nhất các commit từ một branch khác vào branch hiện tại.

git blame -C: Hiển thị lịch sử commit của một file cùng với các thay đổi được sao chép từ các file khác.
git log --graph: Hiển thị lịch sử commit của repository dưới dạng đồ thị để dễ dàng theo dõi.
git stash apply --index: Áp dụng một stash vào branch hiện tại và giữ nguyên các thay đổi đã được stage.
git add -p: Chọn từng phần của các thay đổi trong một file để thêm vào staging area.
git commit --amend: Sửa đổi lại commit message hoặc thêm các thay đổi mới vào commit trước đó.
git log --follow: Hiển thị lịch sử commit của một file theo đường dẫn của nó trong repository.
git grep: Tìm kiếm các chuỗi trong các file trong repository.
git shortlog: Tạo một báo cáo ngắn gọn về lịch sử commit của repository, hiển thị danh sách các tác giả và số lần commit của mỗi tác giả.
git blame -w: Hiển thị lịch sử commit của một file bỏ qua các khoảng trắng.
git rebase -i: Chỉnh sửa lại lịch sử commit của branch hiện tại bằng cách tương tác với một trình biên tập.

```

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

-  `git stash apply stash@{1}`

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

uptime: Hiển thị thời gian hoạt động của hệ thống và thời gian trung bình của các tiến trình đang chạy.
top: Hiển thị các tiến trình đang chạy và thông tin về tài nguyên mà chúng đang sử dụng.
htop: Giống như lệnh top, nhưng với giao diện đồ họa và cho phép tương tác.
free: Hiển thị thông tin về bộ nhớ hệ thống, bao gồm bộ nhớ đã sử dụng, bộ nhớ còn trống và bộ nhớ trao đổi.
df: Hiển thị thông tin về dung lượng ổ đĩa hệ thống, bao gồm dung lượng đã sử dụng và dung lượng còn trống.
du: Hiển thị kích thước của các tệp và thư mục trong hệ thống tệp.
ifconfig: Hiển thị thông tin về các thiết bị mạng, bao gồm địa chỉ IP, địa chỉ MAC và trạng thái kết nối.
netstat: Hiển thị thông tin về các kết nối mạng đang được thiết lập trên hệ thống.
ps: Hiển thị thông tin về các tiến trình đang chạy trên hệ thống, bao gồm ID tiến trình, thời gian chạy và tài nguyên sử dụng.
lsof: Hiển thị danh sách các file đang được mở bởi các tiến trình đang chạy trên hệ thống.

fdisk: Cho phép quản lý các phân vùng trên ổ đĩa.
blkid: Hiển thị thông tin về các phân vùng và các thiết bị lưu trữ được kết nối với hệ thống.
uname: Hiển thị thông tin về phiên bản kernel đang chạy trên hệ thống.
cat /proc/cpuinfo: Hiển thị thông tin về các thông số kỹ thuật của CPU, bao gồm tốc độ xung nhịp, số lõi, và các thông số khác.
lsmod: Hiển thị danh sách các module kernel đang được sử dụng trên hệ thống.
dmesg: Hiển thị các thông báo hạt nhân và hệ thống liên quan đến các sự kiện mới nhất của hệ thống.
journalctl: Hiển thị các thông báo log của hệ thống, bao gồm các thông báo của daemon, ứng dụng và hạt nhân.
ip: Cho phép quản lý các cài đặt mạng, bao gồm địa chỉ IP, subnet mask, route và nhiều hơn nữa.
systemctl: Cho phép quản lý các dịch vụ trên hệ thống, bao gồm khởi động, tắt và khởi động lại dịch vụ.
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
## 20. Port in linux
```
netstat -tulpn
sudo kill -9 <PID/Program name>
```
## 21. Customize theme linux:
```
https://youtu.be/XVuEDsKcFMQ
```
<img
  src="https://user-images.githubusercontent.com/59383987/202881114-847acb26-9e27-404e-a55c-cc4371472512.png"
  min-width="400px"
  max-width="400px"
  width="400px"
  alt="PC"
/>
https://viblo.asia/p/tim-hieu-mongodb-phan-2-Zzb7vDEdRjKd
https://www.reddit.com/r/Ubuntu/comments/kvwuw1/ubuntu_2010_remove_all_password_complexity/


