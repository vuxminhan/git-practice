```Script started on 2023-08-28 16:17:35+07:00 [TERM="dump" TTY="/dev/pts/0" COLUMNS="80" LINES="24"]
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice$ giut  t clone < https://github.com/nnja/advanced-git-exercises.git             alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice$ git clone https://githu>
Cloning into 'advanced-git-exercises'...
remote: Enumerating objects: 28, done.
remote: Counting objects:  33% (1/3)remote: Counting objects:  66% (2/3)remote: Counting objects: 100% (3/3)remote: Counting objects: 100% (3/3), done.
remote: Compressing objects:  33% (1/3)remote: Compressing objects:  66% (2/3)remote: Compressing objects: 100% (3/3)remote: Compressing objects: 100% (3/3), done.
remote: Total 28 (delta 0), reused 0 (delta 0), pack-reused 25
Receiving objects:   3% (1/28)Receiving objects:   7% (2/28)Receiving objects:  10% (3/28)Receiving objects:  14% (4/28)Receiving objects:  17% (5/28)Receiving objects:  21% (6/28)Receiving objects:  25% (7/28)Receiving objects:  28% (8/28)Receiving objects:  32% (9/28)Receiving objects:  35% (10/28)Receiving objects:  39% (11/28)Receiving objects:  42% (12/28)Receiving objects:  46% (13/28)Receiving objects:  50% (14/28)Receiving objects:  53% (15/28)Receiving objects:  57% (16/28)Receiving objects:  60% (17/28)Receiving objects:  64% (18/28)Receiving objects:  67% (19/28)Receiving objects:  71% (20/28)Receiving objects:  75% (21/28)Receiving objects:  78% (22/28)Receiving objects:  82% (23/28)Receiving objects:  85% (24/28)Receiving objects:  89% (25/28)Receiving objects:  92% (26/28)Receiving objects:  96% (27/28)Receiving objects: 100% (28/28)Receiving objects: 100% (28/28), done.
Resolving deltas:   0% (0/1)Resolving deltas: 100% (1/1)Resolving deltas: 100% (1/1), done.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice$ cd  ls
advanced-git-exercises  ex1  ex2  my_output  README.md
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice$ cd advan     <neDrive/lab/git-practice$ cd advanced-git-exercises      
</OneDrive/lab/git-practice/advanced-git-exercises$ ls  ls -a
.  ..  .git  hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git chce  eckout exercise2
Branch 'exercise2' set up to track remote branch 'exercise2' from 'origin'.
Switched to a new branch 'exercise2'
</OneDrive/lab/git-practice/advanced-git-exercises$ git ls-files -s
100644 980a0d5f19a64b4b30a87d4206aade58726b60e3 0hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ echo ""h"e"l"l"o" "a"g"a"i"i"n"" " i"n"" " n"</OneDrive/lab/git-practice/advanced-git-exercises$ echo "hello again"   </OneDrive/lab/git-practice/advanced-git-exercises$ echo "hello again" >> gel</advanced-git-exercises$ echo "hello again" >> gell                         o     hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git status
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")
</OneDrive/lab/git-practice/advanced-git-exercises$ git add -p hello.txt
diff --git a/hello.txt b/hello.txt
index 980a0d5..49fcc02 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1 +1,2 @@
 Hello World!
+hello again
(1/1) Stage this hunk [y,n,q,a,d,e,?]? y

</OneDrive/lab/git-practice/advanced-git-exercises$ git reset
Unstaged changes after reset:
Mhello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git     git status
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")
</OneDrive/lab/git-practice/advanced-git-exercises$ git stash save ""t"r"y" "g"i"t"-"c"" e"</advanced-git-exercises$ git stash save "try git-em"                         e"r"g"e"n"c"y" "c"a"s"t"i"n"g"</advanced-git-exercises$ git stash save "try git-emergency</advanced-git-exercises$ git stash save "try git-emergency </advanced-git-exercises$ git stash save "try git-emergency c</advanced-git-exercises$ git stash save "try git-emergency ca</advanced-git-exercises$ git stash save "try git-emergency cas</advanced-git-exercises$ git stash save "try git-emergency cast</advanced-git-exercises$ git stash save "try git-emergency casti</advanced-git-exercises$ git stash save "try git-emergency castin</advanced-git-exercises$ git stash save "try git-emergency casting</advanced-git-exercises$ git stash save "try git-emergency casting"" " " " " " " " " " " " " " " " " " " " " " " " " e"m"e"r"g"e"n"c"y" "g"i"t"-"c"a"s"t"i"n"g"</advanced-git-exercises$ git stash save "emergency git-casting"
Saved working directory and index state On exercise2: emergency git-casting
</OneDrive/lab/git-practice/advanced-git-exercises$ git statsu  us
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

nothing to commit, working tree clean
</OneDrive/lab/git-practice/advanced-git-exercises$ git sat  tash list
WARNING: terminal is not fully functional
Press RETURN to continue 
stash@{0}: On exercise2: emergency git-casting
</OneDrive/lab/git-practice/advanced-git-exercises$ git stash show stash@{0}
WARNING: terminal is not fully functional
Press RETURN to continue 
 hello.txt | 1 +
 1 file changed, 1 insertion(+)
</OneDrive/lab/git-practice/advanced-git-exercises$ git stash apply stash     stash@{0}
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")
</OneDrive/lab/git-practice/advanced-git-exercises$ git diff hellp o.txt
WARNING: terminal is not fully functional
Press RETURN to continue 
diff --git a/hello.txt b/hello.txt
index 980a0d5..49fcc02 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1 +1,2 @@
 Hello World!
+hello again
</OneDrive/lab/git-practice/advanced-git-exercises$ git     git status
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")
</OneDrive/lab/git-practice/advanced-git-exercises$ git add hello.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git commit -m ad  commit      ""U"p"d"a"t"e" "h"e"l"</advanced-git-exercises$ git commit -m "Update hell"                         o"."t"x"t"</advanced-git-exercises$ git commit -m "Update hello.txt"
[exercise2 342c838] Update hello.txt
 1 file changed, 1 insertion(+)
</OneDrive/lab/git-practice/advanced-git-exercises$ git     exit    e exit
exit

Script done on 2023-08-28 16:24:43+07:00 [COMMAND_EXIT_CODE="0"]
```
