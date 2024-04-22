# Git Exercise

## Bundle 1

### Exercise 1

```bash
The Gym@DESKTOP-9UFVDG8 MINGW64 ~
$ cd desktop

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop (master)
$ mkdir Git-Exercise

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop (master)
$ cd Git-Exercise

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (master)
$ git init
Initialized empty Git repository in C:/Users/The Gym/Desktop/Git-Exercise/.git/

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (master)
$ git branch -M main

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ code .

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git add .

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git commit -m "Add README.md File"
[main (root-commit) 297c68b] Add README.md File
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git remote add origin https://github.com/musi922/Gym-Git-Exercise-Solutions.git

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 225 bytes | 112.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout -b dev
Switched to a new branch 'dev'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (dev)
$ git branch
* dev
  main

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (dev)
$ git checkout -b test
Switched to a new branch 'test'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (test)
$ git checkout dev
Switched to branch 'dev'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (dev)
$ git branch
* dev
  main
  test

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (dev)
$ git branch -d test
Deleted branch test (was 297c68b).

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (dev)
$ git branch
* dev
  main

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$

```
#### Exercise 2

```bash
The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.      

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash list

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash push -m "Home page changes"
Saved working directory and index state On main: Home page changes

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git add .

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash push -m "About page changes"
Saved working directory and index state On main: About page changes

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git add .

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html


The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash push -m "team page changes"
Saved working directory and index state On main: team page changes

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash list
stash@{0}: On main: team page changes
stash@{1}: On main: About page changes
stash@{2}: On main: Home page changes

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (dd32bb45c42d2df9d5adbedbdc683f709b934f4b)

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash list
stash@{0}: On main: team page changes
stash@{1}: On main: Home page changes

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (781dbc7d3599a526187bcae1c949c5e965a2d981)

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git add home.html about.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git commit -m "added home page and about page"
[main 8b1d525] added home page and about page
 2 files changed, 38 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 510 bytes | 510.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
   9a6e168..8b1d525  main -> main

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash list
stash@{0}: On main: team page changes

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (ca050e93bf9d0f1134a5c994da5254f1d3a6d72a)

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git reset --hard HEAD
HEAD is now at 8b1d525 added home page and about page

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)      
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git add .

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git commit -m "Add README.md file changes"
[main d0fb1ea] Add README.md file changes
 1 file changed, 129 insertions(+)

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.49 KiB | 1.49 MiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
   8b1d525..d0fb1ea  main -> main
branch 'main' set up to track 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$
```

## Bundle 2

### Exercise 1

```bash
The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout -b ft/bundle-2 
Switched to a new branch 'ft/bundle-2'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/bundle-2)
$ git add service.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/bundle-2)
$ git commit -m "Add new page Service page"
[ft/bundle-2 1be1688] Add new page Service page
 1 file changed, 19 insertions(+)
 create mode 100644 service.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/bundle-2)
$ git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 490 bytes | 490.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:       
remote:      https://github.com/musi922/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/bundle-2)
$ git checkout main
M       README.md
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git pull origin main
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 911 bytes | 182.00 KiB/s, done.
From https://github.com/musi922/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
   d0fb1ea..7378c99  main       -> origin/main
Updating d0fb1ea..7378c99
Fast-forward
 service.html | 19 +++++++++++++++++++
 1 file changed, 19 insertions(+)
 create mode 100644 service.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git add .

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git commit -m "Added Service Page"
[main 7ac7669] Added Service Page
 1 file changed, 85 insertions(+), 2 deletions(-)

```

### Exercise 2

```bash

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout main
Already on 'main'
Your branch is up to date with 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git pull origin main
From https://github.com/musi922/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Already up to date.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$ git add service.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$ git commit -m "Added Redesign Service Page"
[ft/service-redesign cefc986] Added Redesign Service Page
 1 file changed, 2 deletions(-)

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 302 bytes | 302.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/musi922/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git add .

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git commit -m "Added Changes to Service page"
[main 63be19b] Added Changes to Service page
 1 file changed, 1 insertion(+), 2 deletions(-)

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 302 bytes | 302.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
   f3cbcd2..63be19b  main -> main
branch 'main' set up to track 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$ git diff

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$ git diff main...ft/service-redesign
diff --git a/service.html b/service.html
index 3e04700..42230c8 100644
--- a/service.html
+++ b/service.html
@@ -11,8 +11,6 @@
             <li>Services</li>
             <li>Home</li>
             <li>About</li>
-            <li>News</li>
-            <li>Contact</li>
         </ul>
     </div>
 </body>
 he Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign|MERGING)
$ git add service.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign|MERGING)
$ git commit -m "Resolve Merge conflict with main"
[ft/service-redesign 8a1a3ae] Resolve Merge conflict with main

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 233 bytes | 233.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
   cefc986..8a1a3ae  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/service-redesign)
$
```