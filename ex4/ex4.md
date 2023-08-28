```TERM=dump script my_output
Script started, output log file is 'my_output'.
</OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise4
Your branch is up to date with 'origin/exercise4'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	my_output

nothing added to commit but untracked files present (use "git add" to track)
</OneDrive/lab/git-practice/advanced-git-exercises$ git branch
WARNING: terminal is not fully functional
Press RETURN to continue 
  exercise2
  exercise3
* exercise4
  master
  new
</OneDrive/lab/git-practice/advanced-git-exercises$ git merge exercise3   
Updating 43388fe..e348ebc
Fast-forward
 hello.txt | 1 +
 1 file changed, 1 insertion(+)
</OneDrive/lab/git-practice/advanced-git-exercises$ git log --oneline
WARNING: terminal is not fully functional
Press RETURN to continue 
e348ebc (HEAD -> exercise4, tag: tag-with-anotation, tag: my-exercise3-tag, orig
in/exercise3, exercise3) Testing the emergency git-casting system
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, or
igin/HEAD, master) Initial commit
</OneDrive/lab/git-practice/advanced-git-exercises$ git reset --hard HEAD^
HEAD is now at 43388fe Initial commit
</advanced-git-exercises$ git merge --no-ff exercise3                        
hint: Waiting for your editor to close the file... error: cannot run emacs: No such file or directory
error: unable to start editor 'emacs'
Not committing merge; use 'git commit' to complete the merge.
<advanced-git-exercises$ git branch                 
WARNING: terminal is not fully functional
Press RETURN to continue 
  exercise2
  exercise3
* exercise4
  master
  new
</advanced-git-exercises$ git merge --no-ff exercise3                        
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.
</OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise4
Your branch is up to date with 'origin/exercise4'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
	modified:   hello.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	my_output

</OneDrive/lab/git-practice/advanced-git-exercises$ git stash
Saved working directory and index state WIP on exercise4: 43388fe Initial commit
<advanced-git-exercises$ git merge --no-ff exercise3          
hint: Waiting for your editor to close the file... error: cannot run emacs: No such file or directory
error: unable to start editor 'emacs'
Not committing merge; use 'git commit' to complete the merge.
</OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise4
Your branch is up to date with 'origin/exercise4'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
	modified:   hello.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	my_output

</OneDrive/lab/git-practice/advanced-git-exercises$ ls  
hello.txt  my_output
</OneDrive/lab/git-practice/advanced-git-exercises$ rm my_output
</OneDrive/lab/git-practice/advanced-git-exercises$ ls
hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise4
Your branch is up to date with 'origin/exercise4'.

All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
	modified:   hello.txt

<advanced-git-exercises$ git reset --hard HEAD^         
fatal: ambiguous argument 'HEAD^': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
</OneDrive/lab/git-practice/advanced-git-exercises$ git reset --hard HEAD 
HEAD is now at 43388fe Initial commit
<advanced-git-exercises$ git merge --no-ff exercise3
hint: Waiting for your editor to close the file... error: cannot run emacs: No such file or directory
error: unable to start editor 'emacs'
Not committing merge; use 'git commit' to complete the merge.
</OneDrive/lab/git-practice/advanced-git-exercises$ git commit -m ""
Aborting commit due to empty commit message.
</OneDrive/lab/git-practice/advanced-git-exercises$ git commit -m "ex3 modify"
[exercise4 4d268aa] ex3 modify
</advanced-git-exercises$ git merge --no-ff exercise3
Already up to date.
</OneDrive/lab/git-practice/advanced-git-exercises$ git log --graph
WARNING: terminal is not fully functional
Press RETURN to continue 
*   commit 4d268aadf2fae5e73eb34b6f5c435df7695ac13c (HEAD -> exercise4)
|\  Merge: 43388fe e348ebc
| | Author: vuxminhan <11210261@st.neu.edu.vn>
| | Date:   Mon Aug 28 16:58:16 2023 +0700
| | 
| |     ex3 modify
| | 
| * commit e348ebc1187cb3b4066b1e9432a614b464bf9d07 (tag: tag-with-anotation, ta
g: my-exercise3-tag, origin/exercise3, exercise3)
|/  Author: Nina Zakharenko <nina@nnja.io>
|   Date:   Wed Oct 4 19:01:12 2017 -0700
|   
|       Testing the emergency git-casting system
| 
* commit 43388fee19744e8893467331d7853a6475a227b8 (origin/master, origin/exercis
e7, origin/exercise4, origin/exercise2, origin/HEAD, master)
  Author: Nina Zakharenko <nina@nnja.io>
  Date:   Wed Oct 4 18:51:49 2017 -0700
  
      Initial commit
</OneDrive/lab/git-practice/advanced-git-exercises$ git checkout -b mundo
Switched to a new branch 'mundo'
</OneDrive/lab/git-practice/advanced-git-exercises$ ls  
hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git branch
WARNING: terminal is not fully functional
Press RETURN to continue 
  exercise2
  exercise3
  exercise4
  master
* mundo
  new
</advanced-git-exercises$ echo "Hello Mundo" > hello.txt                     
</OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
Hello Mundo
</OneDrive/lab/git-practice/advanced-git-exercises$ git add hello.txt
</advanced-git-exercises$ git commit -m "Change World to Mundo"               
[mundo 4eed315] Change World to Mundo
 1 file changed, 1 insertion(+), 2 deletions(-)
</OneDrive/lab/git-practice/advanced-git-exercises$ git checkout exercise4
Switched to branch 'exercise4'
Your branch is ahead of 'origin/exercise4' by 2 commits.
  (use "git push" to publish your local commits)
</OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
Hello World!
This is a test of the emergency git-casting system.
</advanced-git-exercises$ echo "Hola World" > hello.txt                      
</OneDrive/lab/git-practice/advanced-git-exercises$ echo hello.txt
hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
Hola World
</OneDrive/lab/git-practice/advanced-git-exercises$ git add hello.txt
</advanced-git-exercises$ git commit -m "Change Hello to Hola"                
[exercise4 0e36b57] Change Hello to Hola
 1 file changed, 1 insertion(+), 2 deletions(-)
</advanced-git-exercises$ git config rerere.enabled true                     
</OneDrive/lab/git-practice/advanced-git-exercises$ git merge mundo
Auto-merging hello.txt
CONFLICT (content): Merge conflict in hello.txt
Recorded preimage for 'hello.txt'
Automatic merge failed; fix conflicts and then commit the result.
</OneDrive/lab/git-practice/advanced-git-exercises$ git rerere diff
--- a/hello.txt
+++ b/hello.txt
@@ -1,5 +1,5 @@
-<<<<<<<
-Hello Mundo
-=======
+<<<<<<< HEAD
 Hola World
->>>>>>>
+=======
+Hello Mundo
+>>>>>>> mundo
</OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
<<<<<<< HEAD
Hola World
=======
Hello Mundo
>>>>>>> mundo
</advanced-git-exercises$ echo "Hola Mundo!" > hello.txt                     
<anced-git-exercises$ rerere diff                    
Command 'rerere' not found, did you mean:
  command 'revere' from snap revere (0.1.4)
See 'snap info <snapname>' for additional versions.
</OneDrive/lab/git-practice/advanced-git-exercises$ git rerere diff
--- a/hello.txt
+++ b/hello.txt
@@ -1,5 +1 @@
-<<<<<<<
-Hello Mundo
-=======
-Hola World
->>>>>>>
+Hola Mundo!
</OneDrive/lab/git-practice/advanced-git-exercises$ git add hello.txt
</advanced-git-exercises$ git commit -m "merge in mundo branch"               
Recorded resolution for 'hello.txt'.
[exercise4 7cea7ac] merge in mundo branch
</OneDrive/lab/git-practice/advanced-git-exercises$ git reset --hard HEAD
HEAD is now at 7cea7ac merge in mundo branch
</OneDrive/lab/git-practice/advanced-git-exercises$ git log --graph
WARNING: terminal is not fully functional
Press RETURN to continue 
*   commit 7cea7ac8e3a65f70a8a14b8bf6e55ae71165ca01 (HEAD -> exercise4)
|\  Merge: 0e36b57 4eed315
| | Author: vuxminhan <11210261@st.neu.edu.vn>
| | Date:   Mon Aug 28 17:06:36 2023 +0700
| | 
| |     merge in mundo branch
| | 
| * commit 4eed315340156eb36807a2a26401cf4aba3e7b80 (mundo)
| | Author: vuxminhan <11210261@st.neu.edu.vn>
| | Date:   Mon Aug 28 17:01:09 2023 +0700
| | 
| |     Change World to Mundo
| | 
* | commit 0e36b5709c70048b9f2cc81c4e0dd7b174739884
|/  Author: vuxminhan <11210261@st.neu.edu.vn>
|   Date:   Mon Aug 28 17:02:20 2023 +0700
|   
|       Change Hello to Hola
|   
*   commit 4d268aadf2fae5e73eb34b6f5c435df7695ac13c
|\  Merge: 43388fe e348ebc
| | Author: vuxminhan <11210261@st.neu.edu.vn>
| | Date:   Mon Aug 28 16:58:16 2023 +0700
</OneDrive/lab/git-practice/advanced-git-exercises$ 
</OneDrive/lab/git-practice/advanced-git-exercises$ git reset --hard HEAD^
HEAD is now at 0e36b57 Change Hello to Hola
</OneDrive/lab/git-practice/advanced-git-exercises$ git merge mundo
Auto-merging hello.txt
CONFLICT (content): Merge conflict in hello.txt
Resolved 'hello.txt' using previous resolution.
Automatic merge failed; fix conflicts and then commit the result.
</OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
Hola Mundo!
</OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise4
Your branch is ahead of 'origin/exercise4' by 3 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
	both modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")
</OneDrive/lab/git-practice/advanced-git-exercises$ git add hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
Hola Mundo!
</advanced-git-exercises$ git commit -m "stage resolved file by rerere"       
[exercise4 0a53a8f] stage resolved file by rerere
</OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise4
Your branch is ahead of 'origin/exercise4' by 5 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
</OneDrive/lab/git-practice/advanced-git-exercises$ exit
exit
Script done.
```
