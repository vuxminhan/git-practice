```
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git checkout exercise6
Branch 'exercise6' set up to track remote branch 'exercise6' from 'origin'.
Switched to a new branch 'exercise6'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ echo "Wrong entries" > hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.template
Wrong entries
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git checkout -- hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ ls
hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.template
[greeting] [noun]!
This is a test of the emergency git-casting system.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --name-status --follow --oneline hello.template
4b2b90e (HEAD -> exercise6, origin/exercise6) Replacing greeting with tokens for i18n
R073    hello.txt       hello.template
fec9e7b Changing Hello to Hola
M       hello.txt
afa34a6 Changing World to Mundo
M       hello.txt
e348ebc (tag: tag-with-anotation, tag: my-exercise3-tag, origin/exercise3, exercise3) Testing the emergency git-casting system
M       hello.txt
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master) Initial commit
A       hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git checkout fec9e7b -- hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ ls
hello.template  hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
Hola World!
This is a test of the emergency git-casting system.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git reset HEAD hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise6
Your branch is up to date with 'origin/exercise6'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	hello.txt

nothing added to commit but untracked files present (use "git add" to track)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git rm mhello.template
fatal: pathspec 'mhello.template' did not match any files
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git rm hello.template
rm 'hello.template'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise6
Your branch is up to date with 'origin/exercise6'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	deleted:    hello.template

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	hello.txt

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git commit -m "Delete hello.template"
[exercise6 74d2081] Delete hello.template
 1 file changed, 2 deletions(-)
 delete mode 100644 hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --name-status --follow --oneline hello.template
fatal: ambiguous argument 'hello.template': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --diff-filter=D --oneline hello.template
fatal: ambiguous argument 'hello.template': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --diff-filter=D --oneline -- hello.template
74d2081 (HEAD -> exercise6) Delete hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git checkout 74d2081 -- hello.template
error: pathspec 'hello.template' did not match any file(s) known to git
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git checkout 74d2081^ -- hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise6
Your branch is ahead of 'origin/exercise6' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   hello.template

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	hello.txt

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.template
[greeting] [noun]!
This is a test of the emergency git-casting system.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git clean --dry-run
Would remove hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git clean -f
Removing hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise6
Your branch is ahead of 'origin/exercise6' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   hello.template

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git reset -- hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ sgit status
Command 'sgit' not found, did you mean:
  command 'jgit' from deb jgit-cli (4.11.9-1)
  command 'dgit' from deb dgit (9.15)
  command 'git' from deb git (1:2.34.1-1ubuntu1.10)
  command 'qgit' from deb qgit (2.10-2)
Try: sudo apt install <deb name>
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise6
Your branch is ahead of 'origin/exercise6' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	hello.template

nothing added to commit but untracked files present (use "git add" to track)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --oneline
74d2081 (HEAD -> exercise6) Delete hello.template
4b2b90e (origin/exercise6) Replacing greeting with tokens for i18n
ff91b70 (origin/exercise5) Merging in mundo branch
fec9e7b Changing Hello to Hola
4582f72 Merge branch 'exercise3' into exercise4
afa34a6 Changing World to Mundo
7ea8b01 Merge branch 'exercise3' into exercise4
e348ebc (tag: tag-with-anotation, tag: my-exercise3-tag, origin/exercise3, exercise3) Testing the emergency git-casting system
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ ls
hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ rm hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git reset 4b2b90e -- hello.template
Unstaged changes after reset:
D	hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise6
Your branch is ahead of 'origin/exercise6' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   hello.template

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	deleted:    hello.template

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.template
cat: hello.template: No such file or directory
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ ls
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git reset --hard HEAD
HEAD is now at 74d2081 Delete hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log -2 --oneline
74d2081 (HEAD -> exercise6) Delete hello.template
4b2b90e (origin/exercise6) Replacing greeting with tokens for i18n
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git reset 4b2b90e
Unstaged changes after reset:
D	hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log -1 --oneline
4b2b90e (HEAD -> exercise6, origin/exercise6) Replacing greeting with tokens for i18n
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git reset ORIG_HEAD
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log -1 --oneline
74d2081 (HEAD -> exercise6) Delete hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git revert 713f6a1
fatal: bad revision '713f6a1'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git revert 74d2081
[exercise6 a0aff80] Revert "Delete hello.template"
 1 file changed, 2 insertions(+)
 create mode 100644 hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --graph
* commit a0aff80725721f2738e5cf795b9d304d2728acb7 (HEAD -> exercise6)
| Author: vuxminhan <11210261@st.neu.edu.vn>
| Date:   Mon Aug 28 23:07:55 2023 +0700
| 
|     Revert "Delete hello.template"
|     
|     This reverts commit 74d20818de9c8fbd850ef78aa29979d94a1a650e.
| 
* commit 74d20818de9c8fbd850ef78aa29979d94a1a650e
| Author: vuxminhan <11210261@st.neu.edu.vn>
| Date:   Mon Aug 28 22:56:38 2023 +0700
| 
|     Delete hello.template
| 
* commit 4b2b90ec4f526139ca9c81e22174ebf5b9c56b52 (origin/exercise6)
| Author: Nina Zakharenko <nina@nnja.io>
| Date:   Wed Oct 4 20:46:45 2017 -0700
| 
|     Replacing greeting with tokens for i18n
|     
|     Currently, hello.txt contains both Spanish and English.
|     Let's replace Hola with a [greeting] token, and Mundo
|     with a [noun] token. That way, we can localize hello.txt for
```
