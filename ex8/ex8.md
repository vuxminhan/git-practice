```
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote -v
origin	https://github.com/vuxminhan/advanced-git-exercises.git (fetch)
origin	https://github.com/vuxminhan/advanced-git-exercises.git (push)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote rename origin upstream
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote rename origin upstream
error: No such remote: 'origin'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote -v
upstream	https://github.com/vuxminhan/advanced-git-exercises.git (fetch)
upstream	https://github.com/vuxminhan/advanced-git-exercises.git (push)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote add origin https://github.com/vuxminhan/advanced-git-exercises-fork.git
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote -v
origin	https://github.com/vuxminhan/advanced-git-exercises-fork.git (fetch)
origin	https://github.com/vuxminhan/advanced-git-exercises-fork.git (push)
upstream	https://github.com/vuxminhan/advanced-git-exercises.git (fetch)
upstream	https://github.com/vuxminhan/advanced-git-exercises.git (push)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git status
On branch main
Your branch is up to date with 'upstream/main'.

nothing to commit, working tree clean
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git checkout master
Branch 'master' set up to track remote branch 'master' from 'upstream'.
Switched to a new branch 'master'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch --set-upstream-to origin/master
error: the requested upstream branch 'origin/master' does not exist
hint: 
hint: If you are planning on basing your work on an upstream
hint: branch that already exists at the remote, you may need to
hint: run "git fetch" to retrieve it.
hint: 
hint: If you are planning to push out a new local branch that
hint: will track its remote counterpart, you may want to use
hint: "git push -u" to set the upstream config as you push.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch --set-upstream-to origin/main
error: the requested upstream branch 'origin/main' does not exist
hint: 
hint: If you are planning on basing your work on an upstream
hint: branch that already exists at the remote, you may need to
hint: run "git fetch" to retrieve it.
hint: 
hint: If you are planning to push out a new local branch that
hint: will track its remote counterpart, you may want to use
hint: "git push -u" to set the upstream config as you push.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch
  exercise2
  exercise3
  exercise4
  exercise5
  exercise6
  exercise7
  exercise7-2
  main
* master
  mundo
  new
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch -u upstream/master master
Branch 'master' set up to track remote branch 'master' from 'upstream'.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch -u origin/master master
error: the requested upstream branch 'origin/master' does not exist
hint: 
hint: If you are planning on basing your work on an upstream
hint: branch that already exists at the remote, you may need to
hint: run "git fetch" to retrieve it.
hint: 
hint: If you are planning to push out a new local branch that
hint: will track its remote counterpart, you may want to use
hint: "git push -u" to set the upstream config as you push.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote-v
git: 'remote-v' is not a git command. See 'git --help'.

The most similar command is
	remote-fd
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git remote -v
origin	https://github.com/vuxminhan/advanced-git-exercises-fork.git (fetch)
origin	https://github.com/vuxminhan/advanced-git-exercises-fork.git (push)
upstream	https://github.com/vuxminhan/advanced-git-exercises.git (fetch)
upstream	https://github.com/vuxminhan/advanced-git-exercises.git (push)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch -u upstream/master master
Branch 'master' set up to track remote branch 'master' from 'upstream'.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch -u origin/master master
error: the requested upstream branch 'origin/master' does not exist
hint: 
hint: If you are planning on basing your work on an upstream
hint: branch that already exists at the remote, you may need to
hint: run "git fetch" to retrieve it.
hint: 
hint: If you are planning to push out a new local branch that
hint: will track its remote counterpart, you may want to use
hint: "git push -u" to set the upstream config as you push.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch
  exercise2
  exercise3
  exercise4
  exercise5
  exercise6
  exercise7
  exercise7-2
  main
* master
  mundo
  new
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git pull origin master

From https://github.com/vuxminhan/advanced-git-exercises-fork
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master
Already up to date.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ 
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch --set-upstream-to origin/master
Branch 'master' set up to track remote branch 'master' from 'origin'.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git checkout -b feature
Switched to a new branch 'feature'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ ls
hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ echo "Changes to local repo" > local_change.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git add local_change.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git commit -m "Change to local repo"
[feature 04ef8cc] Change to local repo
 1 file changed, 1 insertion(+)
 create mode 100644 local_change.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git pull --rebase upstream master
fatal: couldn't find remote ref master
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git pull --rebase upstream main
From https://github.com/vuxminhan/advanced-git-exercises
 * branch            main       -> FETCH_HEAD
Successfully rebased and updated refs/heads/feature.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git log --oneline
25a6585 (HEAD -> feature) Change to local repo
a0c2c83 (upstream/main, main) new updates added to master
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, master) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git pull --rebase
There is no tracking information for the current branch.
Please specify which branch you want to rebase against.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=<remote>/<branch> feature

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ branch
Command 'branch' not found, but can be installed with:
sudo apt install rheolef
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch
  exercise2
  exercise3
  exercise4
  exercise5
  exercise6
  exercise7
  exercise7-2
* feature
  main
  master
  mundo
  new
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'upstream/main'.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git pull --rebase
Already up to date.

```
