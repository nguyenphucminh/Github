## Guide GitHub: 
1. How To Install GitBash:

- Install this file: [Link GitBash](https://git-scm.com/download/win)

2. Open CMD or powershell:

- Config Username: 
   ` git config --global user.name "username Github"`
- Config Gmail: 
   ` git config --global user.email "gmail"`
  
3. How to create a new repository 

- `git init`

4. How to clone a repository 

- `git clone http://github.com/username/filename.git (copy URL)`

5. GUIDE
Review the changes use git status

Add all the changes of you git add .

And then git status (check)

Confirm your changes EX: git commit -m MINH(name) git commit -m ... git commit

Push your new branch to github EX: git push --set-upstream origin MINH(name) git push --set-upstream origin ...

Go to github Website -> Repositories -> Pull requests -> Merge

Go to CMD -> 4.Update branch main git pull origin main
Readmore: https://realfavicongenerator.net/faq#.YuorLnbP02w
Readmore: Common file validation: https://www.validbot.com/tests.php
Create an icon combo:


Go to: https://www.favicon-generator.org/


Choose a file PNG or JPG with size 32x32


Check box with options: Generate icons for Web, Maintain Image Dimensions and Include your favicon.ico in the public gallery


Press Create Favicon


Click on the link "Download the generated favicon" to dowload


Another link: https://favicon.io/
Link test: https://realfavicongenerator.net/
NOTE: You don't need to create new branch, for that you can push directly to main branch. When you push to main branch, you won't need to merge. git push origin main.

NOTE: Delete file or folder on Repositories EX: git rm A.docx (filename) git rm ...

NOTE: Use "git log" command can help you to review history OR Less content use "git log --oneline"

NOTE: Use "git restore ." command can help you restore all file since last commit

NOTE: Use "git diff" command to review changes since last commit, (compare changed files) OR "git diff -- staged"

6. STASH SAVE

   `git stash save`
   
   `git add .`
   
   `git commit - m `
   
   `git push`
   
   `git stash pop`
   
Some stash advanced:

git stash list: show list stash

git stash drop @{1}: delete stash {1}

git stash clear: delete all stash
