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

## <span style="color:#79A7D3"> Bundle 3</span>

### <span style="color:#EEA47FFF">Exercise 1</span>

```bash
Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add team.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "adding the team page"
[ft/team-page f6f7c2d] adding the team page
 1 file changed, 16 insertions(+)
 create mode 100644 team.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 627 bytes | 627.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/arjorb/Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git log
commit f6f7c2d95e8c6b18d9aedc65fca44d9be8478e6a (HEAD -> ft/team-page, origin/ft/team-page)
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 17:34:35 2022 +0200

    adding the team page

commit d223162d63bdb9d2d4cdff05d3d756db0885810c (origin/main, main, ft/contact-page)
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 16:23:52 2022 +0200

    Add the services that we offer on Monday

commit b1103ce05032aad819c6234cde5c856316bc8ddd
Merge: 940a5ed 9afe941
Author: Chrissie <chrissiemhrk@gmail.com>
Date:   Wed Nov 9 12:07:21 2022 +0200

    Merge pull request #1 from arjorb/ft/bundle-2

    Git Exercise Solution Bundle 2 Exercise 1

commit 9afe941620d60135eec30d58b39f01fd54494830 (origin/ft/bundle-2, ft/bundle-2)
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 10:15:26 2022 +0200

    done working on exercise 1 bundle 2

commit c7bd139533f8e57936838d46ee1b0475aa4de4e1
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 10:10:53 2022 +0200

    add the services page

commit 830660e9edc155aae868aa211f3665b1699e9b23 (origin/dev, dev)
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 09:02:37 2022 +0200

    done exercise 2 on bundle 1

commit 85957ff4948ded33dc9d0b4f1cd3cb804970bb1f
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 08:54:07 2022 +0200

    done working on home and about pages

commit a68b246243f7c1b78bdb3273a6c53f0b101246c8
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 08:40:51 2022 +0200

    done exercise 1 on bundle 1

commit 940a5ed8eb24d0b02df97072c77ccba896de244e
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 07:58:03 2022 +0200

    initial commit

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git cherry-pick f6f7c2d95e8c6b18d9aedc65fca44d9be8478e6a
[ft/contact-page c02c846] adding the team page
 Date: Wed Nov 9 17:34:35 2022 +0200
 1 file changed, 16 insertions(+)
 create mode 100644 team.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add .

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "adding the contact page"
[ft/contact-page 8b35a73] adding the contact page
 1 file changed, 16 insertions(+)
 create mode 100644 contact.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 887 bytes | 443.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/arjorb/Git-Exercise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git add .

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git commit -m "adding the faq page"
[ft/faq-page 2043af3] adding the faq page
 1 file changed, 16 insertions(+)
 create mode 100644 faq.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 627 bytes | 627.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/arjorb/Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/arjorb/Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git log
commit 2043af3152164d142dde472c4180dd76be1ccb22 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 18:01:31 2022 +0200

    adding the faq page

commit 8b35a73657ac02a771c9e63d69c358263ae41782 (origin/ft/contact-page, ft/contact-page)
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 17:56:32 2022 +0200

    adding the contact page

commit c02c846496a541a4f2442f3d74b477b94beb117b
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 17:34:35 2022 +0200

    adding the team page

commit d223162d63bdb9d2d4cdff05d3d756db0885810c (origin/main, main)
Author: John U <arjorb@gmail.com>
Date:   Wed Nov 9 16:23:52 2022 +0200

    Add the services that we offer on Monday

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git revert c02c846496a541a4f2442f3d74b477b94beb117b
[ft/faq-page 9770628] Revert "adding the team page"
 1 file changed, 16 deletions(-)
 delete mode 100644 team.html

Jojos-MacBook-Pro:Gym-Git-Exercise-Solutions arjo$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 269 bytes | 269.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/arjorb/Git-Exercise-Solutions.git
   2043af3..9770628  ft/faq-page -> ft/faq-page


```
