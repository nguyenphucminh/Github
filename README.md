# Github
Github User Guide
Dowload GITBASH for win and install this file
https://git-scm.com/download/win

open CMD or powershell
git config --global user.name <username Github>
git config --global user.email <gmail>

New repository -> add a README file (auto have branch main)
New repository -> not choice (create branch) -> CMD -> git checkout -b main

Start:
1. Convert hard drive containing the folder.
D: 

2. Find the folder
dir

3. Let's use move command to go the folder you want - EX: cd Github
cd
git status (check)

4. Update branch main
git pull origin main

5. Create new branch EX: git checkout -b MINH(name)
git checkout -b ...
git checkout main

6. Add all the changes of you
git add .

7. Confirm your changes EX: git commit -m MINH(name)
git commit -m ...
git commit

8. Push your new branch to github EX: git push --set-upstream origin MINH(name)
git push --set-upstream origin ...

9. Go to github Website -> Repositories -> Pull requests -> Merge

10. Go to CMD -> 4.Update branch main
git pull origin main

NOTE: You don't need to create new branch, for that you can push directly to main branch.
When you push to main branch, you won't need to merge.

git push origin main.


