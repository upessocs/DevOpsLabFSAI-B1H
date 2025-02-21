# DevOps Lab 5

## Name: Rishitt Gupta  
**SAP ID:** 500107002  
**Enrollment Number:** R2142220352  
**Batch:** Full Stack AI B1 Hons  

## GIT Sub Modules  

**You added a Git submodule named JS, which clones the repository https://github.com/DivyaDarshanTiwari/JS.git into your project. Git warns that line endings in .gitmodules will change from LF to CRLF when modified on Windows.**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git submodule add https://github.com/DivyaDarshanTiwari/JS.git
Cloning into 'C:/Users/LENOVO/Desktop/Semester 6/DevLab/LAB-3/HTML/JS'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.
warning: in the working copy of '.gitmodules', LF will be replaced by CRLF the next time Git touches it

**You added a Git submodule (JS), which modified .gitmodules. The submodule is staged for commit, but index.html has unstaged changes.**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
modified: .gitmodules
new file: JS

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: index.html

**You committed the submodule (JS), the .gitmodules file, and changes in index.html, linking the JS repository to your project:-**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
modified: .gitmodules
new file: JS

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: index.html

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git add .

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git commit -m "connected the files and added the js repo"
[main bcae6de] connected the files and added the js repo
3 files changed, 6 insertions(+), 2 deletions(-)
create mode 160000 JS

**You successfully pushed your changes to the remote repository, including the JS submodule, .gitmodules file, and updates to index.html. 🚀:-**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 550 bytes | 275.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/DivyaDarshanTiwari/HTML.git
85169e6..bcae6de main -> main

**You initialized the submodule in your repository. This prepares Git to recognize and manage the submodule (JS) but does not update or fetch its content yet:-**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git submodule init

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ ls
README.md index.html

**You added the CSS repository as a submodule in your project, updating the .gitmodules file. Now, commit the changes and push them to keep the submodule tracked. Run git submodule update --init --recursive if needed. 🚀:-**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git submodule add https://github.com/DivyaDarshanTiwari/CSS.git
Cloning into 'C:/Users/LENOVO/Desktop/Semester 6/DevLab/LAB-3/HTML/CSS'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 3 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (6/6), done.
warning: in the working copy of '.gitmodules', LF will be replaced by CRLF the next time Git touches it

**You successfully added the CSS repository as a submodule and committed the changes. Next, push the commit to sync it with the remote repository. 🚀:-**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git submodule
c48537314e69d7ffba1ed5341ccc09063d4cf626 CSS (heads/main)

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
new file: .gitmodules
new file: CSS

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git commit -m "added the css repo as submodule"
[main 85169e6] added the css repo as submodule
2 files changed, 4 insertions(+)
create mode 100644 .gitmodules
create mode 160000 CSS

**CSS submodule addition has been successfully pushed to the remote repository. 🎉:-**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 449 bytes | 449.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/DivyaDarshanTiwari/HTML.git
13e233d..85169e6 main -> main

*Added **JS* and *CSS* repositories as submodules in the main HTML project, initializing and committing changes related to .gitmodules. Staged, committed, and pushed all modifications to the remote repository. Verified the status using git status, git log, and git submodule to ensure proper linking and updates. Successfully integrated and pushed all changes to GitHub. 🚀:-**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git log
commit 13e233d0cc9c631d833075f64ee002c64dd3f62a (HEAD -> main, origin/main, origin/HEAD)
Author: DivyaDarshanTiwari <davidrocco400@outlook.com>
Date: Fri Feb 7 14:27:07 2025 +0530

    index.html added

commit 7e6e2a9758a475bd060a633270e54ba76c35f690
Author: Divya Darshan Tiwari <125484682+DivyaDarshanTiwari@users.noreply.github.com>
Date: Fri Feb 7 14:17:48 2025 +0530

    Initial commit

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git submodule add https://github.com/DivyaDarshanTiwari/JS.git
Cloning into 'C:/Users/LENOVO/Desktop/Semester 6/DevLab/LAB-3/HTML/JS'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.
warning: in the working copy of '.gitmodules', LF will be replaced by CRLF the next time Git touches it

*You successfully added the **JS* repository as a submodule, staged and committed changes, and pushed them to GitHub. The .gitmodules file was updated, and modifications to index.html were included. The push operation completed successfully, syncing the latest changes to the remote repository. 🚀**

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
modified: .gitmodules
new file: JS

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: index.html

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git add .

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git commit -m "connected the files and added the js repo"
[main bcae6de] connected the files and added the js repo
3 files changed, 6 insertions(+), 2 deletions(-)
create mode 160000 JS

LENOVO@DIVYA16 MINGW64 ~/Desktop/Semester 6/DevLab/LAB-3/HTML (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 550 bytes | 275.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/DivyaDarshanTiwari/HTML.git
85169e6..bcae6de main -> main