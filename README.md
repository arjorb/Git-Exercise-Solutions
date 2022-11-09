# Git Exercise Solution

## <span style="color:#79A7D3"> Bundle 1</span>

### <span style="color:#EEA47FFF">Exercise 1</span>

```bash
Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /Users/arjo/Desktop/Git Commands & Git Flow/Gym-Git-Exercise-Solutions/.git/

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git branch -M main

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add README.md

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "initial commit"
[main (root-commit) 940a5ed] initial commit
 1 file changed, 5 insertions(+)
 create mode 100644 README.md

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git remote add origin https://github.com/arjorb/Git-Exercise-Solutions.git

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 298 bytes | 99.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout -b dev
Switched to a new branch 'dev'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/arjorb/Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      dev -> dev

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout -b test
Switched to a new branch 'test'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/arjorb/Git-Exercise-Solutions/pull/new/test
remote:
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      test -> test

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout dev
M       README.md
Switched to branch 'dev'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git branch -D test
Deleted branch test (was 940a5ed).

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin --delete test
To https://github.com/arjorb/Git-Exercise-Solutions.git
 - [deleted]         test


```

### <span style="color:#EEA47FFF">Exercise 2</span>

```bash
Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add .

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash
Saved working directory and index state WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash list
stash@{0}: WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add about.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash
Saved working directory and index state WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash list
stash@{0}: WIP on dev: a68b246 done exercise 1 on bundle 1
stash@{1}: WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add team.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash
Saved working directory and index state WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash list
stash@{0}: WIP on dev: a68b246 done exercise 1 on bundle 1
stash@{1}: WIP on dev: a68b246 done exercise 1 on bundle 1
stash@{2}: WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (6a918fb0f3b0e11fee0b361d3077b20e6f23d598)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash list
stash@{0}: WIP on dev: a68b246 done exercise 1 on bundle 1
stash@{1}: WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (0a33c5e807d3f6592a12d72ba43de9bb0a46aae3)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "done working on home and about pages"
[dev 85957ff] done working on home and about pages
 2 files changed, 32 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 739 bytes | 369.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/arjorb/Git-Exercise-Solutions.git
   a68b246..85957ff  dev -> dev

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash
No local changes to save

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash list
stash@{0}: WIP on dev: a68b246 done exercise 1 on bundle 1

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (1a14f23f77dd30a05f436087e8882e41ca14a1f9)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git reset --hard
HEAD is now at 85957ff done working on home and about pages

```

## <span style="color:#79A7D3"> Bundle 2</span>

### <span style="color:#EEA47FFF">Exercise 1</span>

```bash
Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout - ft/bundle-2
error: pathspec '-' did not match any file(s) known to git
error: pathspec 'ft/bundle-2' did not match any file(s) known to git

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add .

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "add the services page"
[ft/bundle-2 c7bd139] add the services page
 2 files changed, 20 insertions(+), 1 deletion(-)
 create mode 100644 services.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/bundle-2
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 753 bytes | 753.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/arjorb/Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

```

### <span style="color:#EEA47FFF">Exercise 2</span>

```bash

940a5ed..b1103ce  main       -> origin/main
Updating 940a5ed..b1103ce
Fast-forward
 README.md     | 240 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 about.html    |  16 ++++++++
 home.html     |  16 ++++++++
 services.html |  16 ++++++++
 4 files changed, 288 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add .

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "add the service we provide and welcome messege"
[ft/service-redesign 95fe683] add the service we provide and welcome messege
 1 file changed, 2 insertions(+), 1 deletion(-)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 363 bytes | 363.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/arjorb/Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add .

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit "Add the services that we offer on Monday"
error: pathspec 'Add the services that we offer on Monday' did not match any file(s) known to git

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "Add the services that we offer on Monday"
[main d223162] Add the services that we offer on Monday
 1 file changed, 2 insertions(+), 1 deletion(-)

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 373 bytes | 373.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/arjorb/Git-Exercise-Solutions.git
   b1103ce..d223162  main -> main

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git diff main..ft/service-redesign
diff --git a/services.html b/services.html
index 8a1be4e..d6dfca7 100644
--- a/services.html
+++ b/services.html
@@ -11,7 +11,7 @@
     <title>Git Exercise Solution | Services</title>
   </head>
   <body>
-    <h2>Services that we offer on Monday</h2>
-    <p>Monday is the Best day to go with Energy</p>
+    <h2>Services that we offer & deliver</h2>
+    <div>Youre all welcome</div>
   </body>
 </html>

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch ft/service-redesign
nothing to commit, working tree clean

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/service-redesign
Everything up-to-date

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch ft/service-redesign
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit
U       services.html
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch ft/service-redesign
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   services.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit

hint: Waiting for your editor to close the file...

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git status
On branch ft/service-redesign
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        modified:   services.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit
[ft/service-redesign 223c950] Merge branch 'main' into ft/service-redesign

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 235 bytes | 235.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/arjorb/Git-Exercise-Solutions.git
   95fe683..223c950  ft/service-redesign -> ft/service-redesign

```
