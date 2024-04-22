# Gym-Git-Exercise-Solutions

This file contains the commands executed for the exercises

## Bundle 1

### Exercise 1

```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % history
  169  mkdir git-exercise
  170  clear
  171  ls
  172  cd git-exercise
  173  git init
  174  git status
  175  git add -A
  176  git commit -m "project init and readme"
  177  git remote add origin https://github.com/aimee-annabelle/TheGymGitExercises.git
  178  git push origin --set-upstream main
  179  git checkout -b dev
  180  git push origin --set-upstream dev
  181  git checkout -b test
  182  git push origin --set-upstream test
  183  git checkout dev
  184  git branch -d test
  185  git push origin -d test
ojemba@MacBook-Pro-von-ojemba git-exercise % 
```
### Exercise 2

```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % git add home.html 
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash save "home page stash"
Saved working directory and index state On dev: home page stash
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash list
stash@{0}: On dev: home page stash
ojemba@MacBook-Pro-von-ojemba git-exercise % git add about.html  
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash save "about page stash"
Saved working directory and index state On dev: about page stash
ojemba@MacBook-Pro-von-ojemba git-exercise % git add team.html 
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash save "team page stash"
Saved working directory and index state On dev: team page stash
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash list
stash@{0}: On dev: team page stash
stash@{1}: On dev: about page stash
stash@{2}: On dev: home page stash
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   about.html

Dropped stash@{1} (f4e70479a30c592590e861a02734e6ee824ed208)
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash list
stash@{0}: On dev: team page stash
stash@{1}: On dev: home page stash
ojemba@MacBook-Pro-von-ojemba git-exercise % git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   about.html
	new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

Dropped stash@{1} (bba2d77ae7ef8bb67cba1e9bd8b28c42243ed8d1)
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "home and about pages stashed and poped"
[dev de5cd60] home and about pages stashed and poped
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin --set-upstream dev

ojemba@MacBook-Pro-von-ojemba git-exercise % git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

Dropped refs/stash@{0} (bfd052a9acac42b92fa3809b418d33b57cd5373d)
ojemba@MacBook-Pro-von-ojemba git-exercise % git reset --hard
HEAD is now at de5cd60 home and about pages stashed and poped
```
## Bundle 2

### Exercise 1

```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
ojemba@MacBook-Pro-von-ojemba git-exercise % git add -A
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "new changes on readme with new file services"
[ft/bundle-2 f3fd68a] new changes on readme with new file services
 2 files changed, 14 insertions(+), 91 deletions(-)
 create mode 100644 services.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/bundle-2
```

### Exercise 2

```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b "ft/service-redesign"
Switched to a new branch 'ft/service-redesign'
ojemba@MacBook-Pro-von-ojemba git-exercise % git add -A
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "updated services page"
[ft/service-redesign c7a4bf8] updated services page
 1 file changed, 1 insertion(+)
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 340 bytes | 340.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/aimee-annabelle/TheGymGitExercises/pull/new/ft/service-redesign
remote: 
To https://github.com/aimee-annabelle/TheGymGitExercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
ojemba@MacBook-Pro-von-ojemba git-exercise % git add services.html 
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "main branch changes on services page"
[main 2d14fb0] main branch changes on services page
 1 file changed, 1 insertion(+)
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 362 bytes | 362.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/aimee-annabelle/TheGymGitExercises.git
   05c16c1..2d14fb0  main -> main
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
ojemba@MacBook-Pro-von-ojemba git-exercise % git diff ft/service-redesign main
diff --git a/services.html b/services.html
index ccf1d0f..9f875a2 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
 </head>
 <body>
     <h1> Services page</h1>
-    <p>New changes to services page</p>
+    <span>Different changes from previous ones</span>
 </body>
 </html>
\ No newline at end of file
ojemba@MacBook-Pro-von-ojemba git-exercise % git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
ojemba@MacBook-Pro-von-ojemba git-exercise % git add services.html 
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "merged with main"
[ft/service-redesign f1b8c72] merged with main
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 218 bytes | 218.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/aimee-annabelle/TheGymGitExercises.git
   c7a4bf8..f1b8c72  ft/service-redesign -> ft/service-redesign
ojemba@MacBook-Pro-von-ojemba git-exercise % 
```
## Bundle 3
### Exercise 1

```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "team page created" 
[ft/team-page 416acee] team page created
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 440 bytes | 440.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/aimee-annabelle/TheGymGitExercises/pull/new/ft/team-page
remote: 
To https://github.com/aimee-annabelle/TheGymGitExercises.git
 * [new branch]      ft/team-page -> ft/team-page
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout ft/team-page
Switched to branch 'ft/team-page'
ojemba@MacBook-Pro-von-ojemba git-exercise % git log 
commit 416aceeaca4474fbc5d4f460c4d243bc543bb4b4 (HEAD -> ft/team-page, origin/ft/team-page)
Author: aimee-annabelle <inezannabelle@gmail.com>
Date:   Mon Apr 22 16:31:36 2024 +0200

    team page created

commit 2d14fb0d7039ae417e1f15b262408258a7a66e38 (origin/main, main, ft/contact-page)
Author: aimee-annabelle <inezannabelle@gmail.com>
Date:   Mon Apr 22 15:57:29 2024 +0200

    main branch changes on services page

commit 05c16c131e7e6fcf24e077dcf5f3a87f55933939
Merge: 14c5cb3 f3fd68a
Author: uwumukiza123 <113632531+uwumukiza123@users.noreply.github.com>
Date:   Mon Apr 22 15:22:08 2024 +0200

    Merge pull request #1 from aimee-annabelle/ft/bundle-2
    
    new changes on readme with new file services

commit f3fd68a8e25540c056493e5c0920616ecf23ff07 (origin/ft/bundle-2, ft/bundle-2)
Author: aimee-annabelle <inezannabelle@gmail.com>
Date:   Mon Apr 22 14:32:08 2024 +0200

    new changes on readme with new file services

commit 14c5cb3612be4955fa7c11390cf7f51b41bd8de0
Author: Annabelle <54577405+aimee-annabelle@users.noreply.github.com>
Date:   Mon Apr 22 14:24:57 2024 +0200

    Update README.md

commit a2041b64a58b846c609eefd87616fd7dd202a2c3 (origin/dev, dev)
Author: aimee-annabelle <inezannabelle@gmail.com>
Date:   Mon Apr 22 14:12:04 2024 +0200

    exercise two done - commands put in README file

commit de5cd6033930e97b06ea58632fb82e8e66f29a82
Author: aimee-annabelle <inezannabelle@gmail.com>
Date:   Mon Apr 22 14:06:58 2024 +0200

    home and about pages stashed and poped

commit 9d26d7948d73b503225a4daf454ea5663e90b7e5
Author: aimee-annabelle <inezannabelle@gmail.com>
Date:   Mon Apr 22 13:03:46 2024 +0200

    exercise on commands

commit f7bb4b9b6dfb1e5d9ce116d7f2ea80934883fae9
Author: aimee-annabelle <inezannabelle@gmail.com>
Date:   Mon Apr 22 13:00:18 2024 +0200

    project init and readme
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout ft/contact-page 
Switched to branch 'ft/contact-page'
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/contact-page
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/aimee-annabelle/TheGymGitExercises/pull/new/ft/contact-page
remote: 
To https://github.com/aimee-annabelle/TheGymGitExercises.git
 * [new branch]      ft/contact-page -> ft/contact-page
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout ft/team-page      
Switched to branch 'ft/team-page'
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout ft/contact-page
Switched to branch 'ft/contact-page'
ojemba@MacBook-Pro-von-ojemba git-exercise % git cherry-pick 416aceeaca4474fbc5d4f460c4d243bc543bb4b4
[ft/contact-page 524a829] team page created
 Date: Mon Apr 22 16:31:36 2024 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git add .
ojemba@MacBook-Pro-von-ojemba git-exercise % giti commit -m "cherry picked team page to contact page branch"
zsh: command not found: giti
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "cherry picked team page to contact page branch" 
On branch ft/contact-page
nothing to commit, working tree clean
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all                                                  
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "cherry picked team page to contact page branch"
[ft/contact-page 842e9a8] cherry picked team page to contact page branch
 1 file changed, 1 insertion(+)
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 717 bytes | 717.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To https://github.com/aimee-annabelle/TheGymGitExercises.git
   2d14fb0..842e9a8  ft/contact-page -> ft/contact-page
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
ojemba@MacBook-Pro-von-ojemba git-exercise % git add -all
error: did you mean `--all` (with two dashes)?
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "faq page"
[ft/faq-page 4cd0913] faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 433 bytes | 433.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/aimee-annabelle/TheGymGitExercises/pull/new/ft/faq-page
remote: 
To https://github.com/aimee-annabelle/TheGymGitExercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
ojemba@MacBook-Pro-von-ojemba git-exercise % git log --online
fatal: unrecognized argument: --online
ojemba@MacBook-Pro-von-ojemba git-exercise % git log --oneline
4cd0913 (HEAD -> ft/faq-page, origin/ft/faq-page) faq page
842e9a8 (origin/ft/contact-page, ft/contact-page) cherry picked team page to contact page branch
524a829 team page created
2d14fb0 (origin/main, main) main branch changes on services page
05c16c1 Merge pull request #1 from aimee-annabelle/ft/bundle-2
f3fd68a (origin/ft/bundle-2, ft/bundle-2) new changes on readme with new file services
14c5cb3 Update README.md
a2041b6 (origin/dev, dev) exercise two done - commands put in README file
de5cd60 home and about pages stashed and poped
9d26d79 exercise on commands
f7bb4b9 project init and readme
ojemba@MacBook-Pro-von-ojemba git-exercise % git revert 416aceeaca4474fbc5d4f460c4d243bc543bb4b4
CONFLICT (modify/delete): team.html deleted in parent of 416acee (team page created) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 416acee... team page created
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
ojemba@MacBook-Pro-von-ojemba git-exercise % git revert --abort                                 
ojemba@MacBook-Pro-von-ojemba git-exercise % git status
On branch ft/faq-page
nothing to commit, working tree clean
ojemba@MacBook-Pro-von-ojemba git-exercise % git revert 524a829
CONFLICT (modify/delete): team.html deleted in parent of 524a829 (team page created) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 524a829... team page created
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
ojemba@MacBook-Pro-von-ojemba git-exercise % git revert --continue
On branch ft/faq-page
Your branch is up to date with 'origin/ft/faq-page'.

You are currently reverting commit 524a829.
  (all conflicts fixed: run "git revert --continue")
  (use "git revert --skip" to skip this patch)
  (use "git revert --abort" to cancel the revert operation)

nothing to commit, working tree clean
ojemba@MacBook-Pro-von-ojemba git-exercise % git revert 416aceeaca4474fbc5d4f460c4d243bc543bb4b4
CONFLICT (modify/delete): team.html deleted in parent of 416acee (team page created) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 416acee... team page created
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
ojemba@MacBook-Pro-von-ojemba git-exercise % git revert 416aceeaca4474fbc5d4f460c4d243bc543bb4b4
CONFLICT (modify/delete): team.html deleted in parent of 416acee (team page created) and modified in HEAD.  Version HEAD of team.html left in tree.
error: could not revert 416acee... team page created
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git revert --continue".
hint: You can instead skip this commit with "git revert --skip".
hint: To abort and get back to the state before "git revert",
hint: run "git revert --abort".
ojemba@MacBook-Pro-von-ojemba git-exercise % git push
Everything up-to-date
ojemba@MacBook-Pro-von-ojemba git-exercise % 
```
### Exercise 2
```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "changes to home page
dquote> "
[main 35ab3e0] changes to home page
 1 file changed, 9 insertions(+), 8 deletions(-)
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 385 bytes | 385.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/aimee-annabelle/TheGymGitExercises.git
   2d14fb0..35ab3e0  main -> main
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
ojemba@MacBook-Pro-von-ojemba git-exercise % git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "changes in ft/home-page-redesign after rebase to main"
[ft/home-page-redesign 9c061a4] changes in ft/home-page-redesign after rebase to main
 1 file changed, 1 insertion(+)
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 12 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.65 KiB | 1.65 MiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/aimee-annabelle/TheGymGitExercises/pull/new/ft/home-page-redesign
remote: 
To https://github.com/aimee-annabelle/TheGymGitExercises.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
ojemba@MacBook-Pro-von-ojemba git-exercise %
```
## Bundle 4
### Exercise 1

```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
ojemba@MacBook-Pro-von-ojemba git-exercise % git remote add git-copy https://github.com/aimee-annabelle/TheGymGitExercisesCopy.git
ojemba@MacBook-Pro-von-ojemba git-exercise % giit remote -v
zsh: command not found: giit
ojemba@MacBook-Pro-von-ojemba git-exercise % git remote -v 
git-copy	https://github.com/aimee-annabelle/TheGymGitExercisesCopy.git (fetch)
git-copy	https://github.com/aimee-annabelle/TheGymGitExercisesCopy.git (push)
origin	https://github.com/aimee-annabelle/TheGymGitExercises.git (fetch)
origin	https://github.com/aimee-annabelle/TheGymGitExercises.git (push)
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "updates on home page after adding new repo"
[main 249bf92] updates on home page after adding new repo
 1 file changed, 3 insertions(+)
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 376 bytes | 376.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/aimee-annabelle/TheGymGitExercises.git
   35ab3e0..249bf92  main -> main
ojemba@MacBook-Pro-von-ojemba git-exercise % git push git-copy main
Enumerating objects: 30, done.
Counting objects: 100% (30/30), done.
Delta compression using up to 12 threads
Compressing objects: 100% (28/28), done.
Writing objects: 100% (30/30), 5.39 KiB | 2.69 MiB/s, done.
Total 30 (delta 10), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (10/10), done.
To https://github.com/aimee-annabelle/TheGymGitExercisesCopy.git
 * [new branch]      main -> main
ojemba@MacBook-Pro-von-ojemba git-exercise %
```

### Exercise 2

```bash
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b ft/footer
Switched to a new branch 'ft/footer'
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "feat: footer"
[ft/footer 64c9926] feat: footer
 2 files changed, 24 insertions(+), 1 deletion(-)
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/footer
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 513 bytes | 513.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/aimee-annabelle/TheGymGitExercises/pull/new/ft/footer
remote: 
To https://github.com/aimee-annabelle/TheGymGitExercises.git
 * [new branch]      ft/footer -> ft/footer
ojemba@MacBook-Pro-von-ojemba git-exercise % git add --all               
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "new file footer"
[ft/footer 69d2ca4] new file footer
 1 file changed, 11 insertions(+)
 create mode 100644 footer.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/footer      
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 444 bytes | 444.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/aimee-annabelle/TheGymGitExercises.git
   64c9926..69d2ca4  ft/footer -> ft/footer
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
ojemba@MacBook-Pro-von-ojemba git-exercise % git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'
ojemba@MacBook-Pro-von-ojemba git-exercise % git merge --squash ft/footer
Updating 249bf92..69d2ca4
Fast-forward
Squash commit -- not updating HEAD
 README.md   | 24 +++++++++++++++++++++++-
 footer.html | 11 +++++++++++
 home.html   |  1 +
 3 files changed, 35 insertions(+), 1 deletion(-)
 create mode 100644 footer.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git commit -m "squashed footer commits into one"
[ft/squashing 4423ecb] squashed footer commits into one
 3 files changed, 35 insertions(+), 1 deletion(-)
 create mode 100644 footer.html
ojemba@MacBook-Pro-von-ojemba git-exercise % git push origin ft/squashing
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 740 bytes | 740.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/aimee-annabelle/TheGymGitExercises/pull/new/ft/squashing
remote: 
To https://github.com/aimee-annabelle/TheGymGitExercises.git
 * [new branch]      ft/squashing -> ft/squashing
ojemba@MacBook-Pro-von-ojemba git-exercise % git status
On branch ft/squashing
nothing to commit, working tree clean
ojemba@MacBook-Pro-von-ojemba git-exercise %
```

