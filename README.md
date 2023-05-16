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
## exercise2

```bash

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git checkout main 
Switched to branch 'main'

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


Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push -u origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 218 bytes | 109.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Nezerwa/Gym-Git-Exercise-Solutions.git
   654401b..ca44cd0  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Eligrand@Eligrand-Pc MINGW64 ~/Gym-Git-Exercise-Solutions (ft/service-redesign)
$
```