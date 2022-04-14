## Guide GitHub: 
1. How To Install GitBash
-install this file
1. Item 2
1. Item 3
  1. Item 3a
  1. Item 3b
You may be using [Markdown Live Preview](https://markdownlivepreview.com/).
Github User Guide Dowload GITBASH for win and :
https://git-scm.com/download/win

open CMD or powershell git config --global user.name "username Github" git config --global user.email "gmail"

New repository -> add a README file (auto have branch main) New repository -> not choice (create branch) -> CMD -> git checkout -b main

Go to D: -> git clone http://github.com/username/filename.git (copy URL)

Start:

Convert hard drive containing the folder. D:

Find the folder dir

Let's use move command to go the folder you want - EX: cd Github cd

Update branch main git pull origin main

Create new branch EX: git checkout -b MINH(name) git checkout -b ... git checkout main

Review the changes use git status

Add all the changes of you git add .

And then git status (check)

Confirm your changes EX: git commit -m MINH(name) git commit -m ... git commit

Push your new branch to github EX: git push --set-upstream origin MINH(name) git push --set-upstream origin ...

Go to github Website -> Repositories -> Pull requests -> Merge

Go to CMD -> 4.Update branch main git pull origin main

NOTE: You don't need to create new branch, for that you can push directly to main branch. When you push to main branch, you won't need to merge. git push origin main.

NOTE: Delete file or folder on Repositories EX: git rm A.docx (filename) git rm ...

NOTE: Use "git log" command can help you to review history OR Less content use "git log --oneline"

NOTE: Use "git restore ." command can help you restore all file since last commit

NOTE: Use "git diff" command to review changes since last commit, (compare changed files) OR "git diff -- staged"
