# git exercise

## bundle1

### exercise1

```bash

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions
$ git init
Initialized empty Git repository in C:/Users/Eligrand/Gym-Git-Exercise-Solutions/.git/

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (master)
$ git branch -m master main

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add index.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'Add html file'
[main (root-commit) 56f545f] Add html file
 1 file changed, 13 insertions(+)
 create mode 100644 index.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add styles.css

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'Add css file'
[main 6b0cb95] Add css file
 1 file changed, 5 insertions(+)
 create mode 100644 styles.css


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git status
On branch main
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    styles.css

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        style.css

no changes added to commit (use "git add" and/or "git commit -a")


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add style.css

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'Rename css file'
[main fe78299] Rename css file
 1 file changed, 5 insertions(+)
 create mode 100644 style.css

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add index.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'Make changes in html file to test git'
[main 8b89882] Make changes in html file to test git
 1 file changed, 1 insertion(+), 1 deletion(-)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git remote add origin  https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git push  origin main
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 4 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (11/11), 1.16 KiB | 298.00 KiB/s, done.
Total 11 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 + 20cb1b2...8b89882 main -> main (forced update)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git add index.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git commit -m 'Make changes on html file to push dev branch'
[dev 5245071] Make changes on html file to push dev branch
 1 file changed, 1 insertion(+), 1 deletion(-)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 368 bytes | 368.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git checkout -b test
Switched to a new branch 'test'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (test)
$ git checkout dev
Switched to branch 'dev'


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git branch -D test
Deleted branch test (was 5245071).

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$
```

### exercise2

```bash

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git add home.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 610fdd0 Add README file

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git add about.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 610fdd0 Add README file

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git add team.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 610fdd0 Add README file

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 610fdd0 Add README file
stash@{1}: WIP on dev: 610fdd0 Add README file
stash@{2}: WIP on dev: 610fdd0 Add README file

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (43d04f148009eae656814fd4df1f9d6a6f6a25e6)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped stash@{0} (b0511c546582764e1d2d77e0725718309dfc285f)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 610fdd0 Add README file

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git log
commit 610fdd0f80ddcce2c4b6e8264a3b26e30800dc22 (HEAD -> dev, origin/dev)
Author: Nezerwa <eligrand2000@gmail.com>
Date:   Sun May 14 17:55:47 2023 +0200

    Add README file

commit b83ad2a48a9f01bbd3c717c1af9e71ffc85c65eb

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git reset --hard 610fdd0f80ddcce2c4b6e8264a3b26e30800dc22
HEAD is now at 610fdd0 Add README file

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$
```

## bundle2

### exercise1

```bash

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git add services.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m 'Add service.html'
[ft/bundle-2 2acffc8] Add service.html
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 240 bytes | 120.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$
```
## bundle3

## exercise1

```bash

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (dev)
$ git checkout -b ft/bundle-2 
Switched to a new branch 'ft/bundle-2'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git add services.html 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m 'Add service.html'
[ft/bundle-2 2acffc8] Add service.html
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 240 bytes | 120.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2   
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ ^C


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git add README.md 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m'Add Terminal history for Bundle2 exercise1'
[ft/bundle-2 331f3b8] Add Terminal history for Bundle2 exercise1
 1 file changed, 49 insertions(+), 9 deletions(-)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 5, done.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git checkout main 
Switched to branch 'main'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git pull
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 1.81 KiB | 48.00 KiB/s, done.
From https://github.com/Nezerwa/Gym-Git-Exercise-Solutions
   8b89882..3ad295f  main       -> origin/main
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git pull origin main
From https://github.com/Nezerwa/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Updating 8b89882..3ad295f
Fast-forward
 README.md     | 237 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 home.html     |  12 +++
 index.html    |   2 +-
 services.html |  12 +++
 styles.css    |   5 --
 5 files changed, 262 insertions(+), 6 deletions(-)
 create mode 100644 README.md
 create mode 100644 home.html
 create mode 100644 services.html
 delete mode 100644 styles.css

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add services.html 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m 'Add new div'
[ft/service-redesign 654401b] Add new div
 1 file changed, 1 insertion(+), 1 deletion(-)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origi ft/service-redesign
fatal: 'origi' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 164.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main 
Switched to branch 'main'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add services.html 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'Add changes on service.html'
[main def6765] Add changes on service.html
 1 file changed, 1 insertion(+), 1 deletion(-)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 342 bytes | 342.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   3ad295f..def6765  main -> main

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff main 
diff --git a/services.html b/services.html
index f18aca3..81be930 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
     <title>Document</title>
 </head>
 <body>
-  <div>test merge conflict</div>
+    <div class="testing-div"></div>

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git merge main 
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)   
$ git push -u origin ft/service-redesign
Everything up-to-date
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)   
$ git status
On branch ft/service-redesign
Your branch is up to date with 'origin/ft/service-redesign'.

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)   
$ git add .

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)   
$ git push -u origin ft/service-redesign
Everything up-to-date
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)   
$ git commit -m 'Solve merge conflict'
[ft/service-redesign ca44cd0] Solve merge conflict

```
## Bundle3 

## Exercise 1`

```bash

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout -b  ft/team-page
Switched to a new branch 'ft/team-page'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add team.html 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m 'Add team.html'
[ft/team-page 626bc12] Add team.html
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 239 bytes | 119.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/team-page  
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout ft/team-page 
Switched to branch 'ft/team-page'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit 626bc12bc82819d5e47d98a9437083adc01475d5 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Nezerwa <eligrand2000@gmail.com>
Date:   Tue May 16 15:57:03 2023 +0200

    Add team.html

commit f9dc341830bb345ef435630d27848c360ba9f6bf (origin/ft/service-redesign, ft/service-redesign)
Author: Nezerwa <eligrand2000@gmail.com>

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick 626bc12bc82819d5e47d98a9437083adc01475d5
[ft/contact-page 2667825] Add team.html
 Date: Tue May 16 15:57:03 2023 +0200
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add .

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m 'Add changes from ft/team-page'
On branch ft/contact-page
nothing to commit, working tree clean

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 244 bytes | 122.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git checkout -b  ft/faq-page
Switched to a new branch 'ft/faq-page'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add faq.html 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m 'Add faq.html'
[ft/faq-page b661550] Add faq.html
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 467 bytes | 233.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page   
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert 626bc12bc82819d5e47d98a9437083adc01475d5
hint: Waiting for your editor to close the file... Vim: Error reading input, exiting...
Vim: preserving files...
Vim: Finished.
error: There was a problem with the editor 'vi'.
Please supply the message using either -m or -F option.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    team.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add .

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m 'Remove team.html'
[ft/faq-page f20cc6c] Remove team.html
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 225 bytes | 75.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   b661550..f20cc6c  ft/faq-page -> ft/faq-page

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$
```
## Exercise2

```bash


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git add index.html 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git commit -m 'Add new div'
[main efd1223] Add new div
 1 file changed, 1 insertion(+)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git push origin main
Enumerating objects: 9, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 624 bytes | 104.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   040f8bf..dddeab9  main -> main

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/home-page-redesign 
Switched to branch 'ft/home-page-redesign'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git rebase main
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply 4b604b6... Add solution for Bundle3 exercise 1
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".   
Could not apply 4b604b6... Add solution for Bundle3 exercise 1

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign|REBASE 4/4)
$ git rebase main
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase.  If that is the
case, please try
        git rebase (--continue | --abort | --skip)
If that is not the case, please
        rm -fr ".git/rebase-merge"
and run me again.  I am stopping in case you still have something
valuable there.


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign|REBASE 4/4)
$ git rebase --continue
README.md: needs merge
You must edit all merge conflicts and then
mark them as resolved using git add

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign|REBASE 4/4)
$ git rebase --continue
fatal: No rebase in progress?

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git rebase --continue
fatal: No rebase in progress?

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git rebase main
Current branch ft/home-page-redesign is up to date.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git add home.html 

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git commit -m 'Add testing div'
[ft/home-page-redesign 6102c3e] Add testing div
 1 file changed, 1 insertion(+), 1 deletion(-)

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git push origin home-page-redesign
error: src refspec home-page-redesign does not match any
error: failed to push some refs to 'https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git'

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (13/13), 3.23 KiB | 1.08 MiB/s, done.
Total 13 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/Nezerwa/Gym-Git-Exercise-Solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/home-page-redesign)
$
```

##Bundle 4

##Exercise1

```bash

PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git add .
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git commit -m 'add test div'
[main af79f7e] add test div
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git push origin main 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 324 bytes | 162.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   dddeab9..af79f7e  main -> main
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git remote -v
origin  https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git (fetch)
origin  https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git (push)
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git remote add git-copy  https://github.com/Nezerwa/git-copy.git
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git remote -v                            
git-copy        https://github.com/Nezerwa/git-copy.git (fetch)
git-copy        https://github.com/Nezerwa/git-copy.git (push)
origin  https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git (fetch)
origin  https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git (push)
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git remote -v     
git-copy        https://github.com/Nezerwa/git-copy.git (fetch)
git-copy        https://github.com/Nezerwa/git-copy.git (push)
origin  https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git (fetch)
origin  https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git (push)
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions> git push git-copy
Enumerating objects: 58, done.
Counting objects: 100% (58/58), done.
Delta compression using up to 4 threads
Compressing objects: 100% (57/57), done.
Writing objects: 100% (58/58), 9.89 KiB | 440.00 KiB/s, done.
Total 58 (delta 23), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (23/23), done.
To https://github.com/Nezerwa/git-copy.git
 * [new branch]      main -> main
PS C:\Users\Eligrand\Gym-Git-Exercise-Solutions>

```
