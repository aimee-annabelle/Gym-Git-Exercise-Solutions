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


