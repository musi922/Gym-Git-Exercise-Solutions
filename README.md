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

## Bundle 3

### Exercise 1
```bash
The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/team-page)
$ git add team.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/team-page)
$ git commit -m "Added Team Page"
[ft/team-page ac8e600] Added Team Page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/team-page)
$ git push -u origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 442 bytes | 442.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/musi922/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/team-page)
$ git log
commit ac8e60013cb1f2e73026f3f18c75124e43fbae7c (HEAD -> ft/team-page, origin/ft/team-page)
Author: Richard Musime <richardmusime6@gmail.com>
Date:   Mon Apr 22 16:50:43 2024 +0200

    Added Team Page

commit ed390ac42b38e1e88a7709100160c5e775e8738b (origin/main, main, ft/contact-page)
Author: Richard Musime <richardmusime6@gmail.com>
Date:   Mon Apr 22 16:33:43 2024 +0200

    Added Readme.md Changes

commit e3525e3ee978ccaabbd2e482c78781b100f42e17
Merge: 63be19b 8a1a3ae
Author: musi922 <119411002+musi922@users.noreply.github.com>
Date:   Mon Apr 22 16:26:40 2024 +0200

    Merge pull request #2 from musi922/ft/service-redesign

    Added Redesign Service Page

commit 8a1a3aeb2790ef73510a2372edf9eb4304ee059d (origin/ft/service-redesign)
Merge: cefc986 63be19b
Author: Richard Musime <richardmusime6@gmail.com>
Date:   Mon Apr 22 16:25:28 2024 +0200

    Resolve Merge conflict with main

commit 63be19b16fde638f64528c9bbe4a26fcdd4a6f96
Author: Richard Musime <richardmusime6@gmail.com>
Date:   Mon Apr 22 16:13:52 2024 +0200

    Added Changes to Service page

commit cefc986b2518dc320effe01273ad6b03e7a4ddf2
Author: Richard Musime <richardmusime6@gmail.com>
Date:   Mon Apr 22 16:09:13 2024 +0200

    Added Redesign Service Page

commit f3cbcd2c66d00727443ee378f3ef0382d778d1d0
Author: Richard Musime <richardmusime6@gmail.com>
Date:   Mon Apr 22 16:00:08 2024 +0200

    Added Service Page

commit 7ac76694bb0f7d16f950d7a0022a89913c72154b
Author: Richard Musime <richardmusime6@gmail.com>
Date:   Mon Apr 22 15:59:10 2024 +0200

    Added Service Page

commit 7378c99e71041437e636da30629f6c90e24c6b00
Merge: d0fb1ea 1be1688
Author: Gasorekibo <113452888+Gasorekibo@users.noreply.github.com>

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/contact-page)
$ git chery-pick ac8e60013cb1f2e73026f3f18c75124e43fbae7c
git: 'chery-pick' is not a git command. See 'git --help'.

The most similar command is
        cherry-pick

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/contact-page)
$ git cherry-pick ac8e60013cb1f2e73026f3f18c75124e43fbae7c
[ft/contact-page cff66cf] Added Team Page
 Date: Mon Apr 22 16:50:43 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/contact-page)
$ git add contact.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/contact-page)
$ git commit -m "Added contact page"
[ft/contact-page 7af76a3] Added contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/contact-page)
$ git push -u origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 705 bytes | 352.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/musi922/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/faq-page)
$ git add faq.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/faq-page)
$ git commit -m "Added FAQ page"
[ft/faq-page 89e3e1c] Added FAQ page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/faq-page)
$ git push -u origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 444 bytes | 444.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/musi922/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/faq-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git pull oriin main
fatal: 'oriin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git pull origin main
remote: Enumerating objects: 2, done.
remote: Counting objects: 100% (2/2), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 1.74 KiB | 80.00 KiB/s, done.
From https://github.com/musi922/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
   ed390ac..b2a3fcc  main       -> origin/main
Updating ed390ac..b2a3fcc
Fast-forward
 contact.html | 11 +++++++++++
 team.html    | 11 +++++++++++
 2 files changed, 22 insertions(+)
 create mode 100644 contact.html
 create mode 100644 team.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (main)
$ git checkout -b ft/revert-team-changes
Switched to a new branch 'ft/revert-team-changes'

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/revert-team-changes)
$ git revert
usage: git revert [--[no-]edit] [-n] [-m <parent-number>] [-s] [-S[<keyid>]] <commit>...
   or: git revert (--continue | --skip | --abort | --quit)

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    --skip                skip current commit and continue
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    -n, --no-commit       don't automatically commit
    --commit              opposite of --no-commit
    -e, --[no-]edit       edit the commit message
    -s, --[no-]signoff    add a Signed-off-by trailer
    -m, --[no-]mainline <parent-number>
                          select mainline parent
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible
    --[no-]strategy <strategy>
                          merge strategy

    -X, --[no-]strategy-option <option>
                          option for merge strategy
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit
    --[no-]reference      use the 'reference' format to refer to commits


The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/revert-team-changes)
$ git revert ac8e60013cb1f2e73026f3f18c75124e43fbae7c
[ft/revert-team-changes 8f8d3f7] Added team pageRevert "Added Team Page" This reverts commit ac8e60013cb1f2e73026f3f18c75124e43fbae7c.
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/revert-team-changes)
$ git push origin ft/revert-team-changes
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 281 bytes | 281.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/revert-team-changes' on GitHub by visiting:
remote:      https://github.com/musi922/Gym-Git-Exercise-Solutions/pull/new/ft/revert-team-changes
remote:
To https://github.com/musi922/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/revert-team-changes -> ft/revert-team-changes

The Gym@DESKTOP-9UFVDG8 MINGW64 ~/desktop/Git-Exercise (ft/revert-team-changes)
$
```