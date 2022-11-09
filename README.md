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

```
