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