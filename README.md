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
