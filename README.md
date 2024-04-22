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

