```
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git status
On branch exercise7
Your branch is up to date with 'origin/exercise7'.

nothing to commit, working tree clean
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ cat hello.txt
Hello World!
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ echo "fist file" > first.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ echo "second file" > second.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git add first.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git status
On branch exercise7
Your branch is up to date with 'origin/exercise7'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   first.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	second.txt

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git commit -m "Add two new files"
[exercise7 5b8cd4a] Add two new files
 1 file changed, 1 insertion(+)
 create mode 100644 first.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git commit --amend
[exercise7 cff0aa6] Add two new files
 Date: Tue Aug 29 14:15:31 2023 +0700
 1 file changed, 1 insertion(+)
 create mode 100644 first.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git add second.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git commit --amend
[exercise7 bf9cb6f] Commiting two new files
 Date: Tue Aug 29 14:15:31 2023 +0700
 2 files changed, 2 insertions(+)
 create mode 100644 first.txt
 create mode 100644 second.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git status
On branch exercise7
Your branch is ahead of 'origin/exercise7' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git checkout -b exercise7-2
Switched to a new branch 'exercise7-2'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git log --oneline
43388fe (HEAD -> exercise7-2, origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ ls
hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ echo "new feature" > feature.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git add feature.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git commit -m "adding new feature"
[exercise7-2 9fa2807] adding new feature
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ echo "new updates on branch master" >> hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ cat hello.txt
Hello World!
new updates on branch master
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git add hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git commit -m "
> ^C
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git commit -m "new updates added to master"
[master a0c2c83] new updates added to master
 1 file changed, 1 insertion(+)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git checkout exercise7-
error: pathspec 'exercise7-' did not match any file(s) known to git
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git checkout exercise7-2
Switched to branch 'exercise7-2'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git rebase master
Successfully rebased and updated refs/heads/exercise7-2.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git log --oneline
127c6ed (HEAD -> exercise7-2) adding new feature
a0c2c83 (master) new updates added to master
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ echo "another new feature" > another_new_feature.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git add another_new_feature.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git commit -m "add another new feature"
[exercise7-2 d6a55b6] add another new feature
 1 file changed, 1 insertion(+)
 create mode 100644 another_new_feature.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git log -n 3 --oneline
d6a55b6 (HEAD -> exercise7-2) add another new feature
127c6ed adding new feature
a0c2c83 (master) new updates added to master
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git rebase -i a0c2c83
Successfully rebased and updated refs/heads/exercise7-2.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git rebase -i a0c2c83
[detached HEAD e8e2d71] adding 2 new feature
 Date: Tue Aug 29 14:18:28 2023 +0700
 1 file changed, 1 insertion(+)
 create mode 100644 feature.txt
[detached HEAD 43e6ae3] adding 2 new feature
 Date: Tue Aug 29 14:18:28 2023 +0700
 2 files changed, 2 insertions(+)
 create mode 100644 another_new_feature.txt
 create mode 100644 feature.txt
Successfully rebased and updated refs/heads/exercise7-2.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/git-practice/advanced-git-exercises$ git log --oneline
43e6ae3 (HEAD -> exercise7-2) adding 2 new feature
a0c2c83 (master) new updates added to master
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD) Initial commit

```
