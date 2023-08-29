```alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git branch
  exercise2
  exercise3
  exercise4
  exercise5
  exercise6
  exercise7
  exercise7-2
* exercise9
  feature
  main
  master
  mundo
  new
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git grep -e "Python"
python_code.py:# This is a Python file
python_code.py:    print("Welcome to Python!")
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ ls
bash_code.sh  hello.txt  java_code.java  python_code.py
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ echo "More python code" >> python_code.py
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git grep --line-number -e "Python"
python_code.py:1:# This is a Python file
python_code.py:4:    print("Welcome to Python!")
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git grep --line-number -e "python"
python_code.py:3:def python_function():
python_code.py:5:More python code
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git grep --line-number --cached -e "python"
python_code.py:3:def python_function():
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git add python_code.py
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git grep --line-number --cached -e "python"
python_code.py:3:def python_function():
python_code.py:5:More python code
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git checkout pythoncode.py
error: pathspec 'pythoncode.py' did not match any file(s) known to git
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git reset python_code.py
Unstaged changes after reset:
M	python_code.py
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git log --oneline
88f6e28 (HEAD -> exercise9, upstream/exercise9) Adding bash, python, and java code examples
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, master) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git log exercise3 --oneline
e348ebc (tag: tag-with-anotation, tag: my-exercise3-tag, upstream/exercise3, exercise3) Testing the emergency git-casting system
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, master) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git cherry-pick e348ebc
[exercise9 37363ce] Testing the emergency git-casting system
 Author: Nina Zakharenko <nina@nnja.io>
 Date: Wed Oct 4 19:01:12 2017 -0700
 1 file changed, 1 insertion(+)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git log --oneline
37363ce (HEAD -> exercise9) Testing the emergency git-casting system
88f6e28 (upstream/exercise9) Adding bash, python, and java code examples
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, master) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git blame python.py
fatal: no such path 'python.py' in HEAD
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ ls
bash_code.sh  hello.txt  java_code.java  python_code.py
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git blame python_code.py
88f6e286 (Nina Zakharenko   2017-10-05 11:31:34 -0700 1) # This is a Python file
88f6e286 (Nina Zakharenko   2017-10-05 11:31:34 -0700 2) 
88f6e286 (Nina Zakharenko   2017-10-05 11:31:34 -0700 3) def python_function():
88f6e286 (Nina Zakharenko   2017-10-05 11:31:34 -0700 4)     print("Welcome to Python!")
00000000 (Not Committed Yet 2023-08-29 15:17:32 +0700 5) More python code
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git rm java_code.java
rm 'java_code.java'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git commit -m "Delete java code"
[exercise9 6399528] Delete java code
 1 file changed, 7 deletions(-)
 delete mode 100644 java_code.java
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git log --diff-filter=D
commit 63995283ff201961a709878106f9f68b14ff4a48 (HEAD -> exercise9)
Author: vuxminhan <11210261@st.neu.edu.vn>
Date:   Tue Aug 29 15:18:41 2023 +0700

    Delete java code
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git blame 63995283ff201961a709878106f9f68b14ff4a48
fatal: no such path '63995283ff201961a709878106f9f68b14ff4a48' in HEAD
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git blame 63995283ff201961a709878106f9f68b14ff4a48^ 
fatal: no such path '63995283ff201961a709878106f9f68b14ff4a48^' in HEAD
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git blame 63995283ff201961a709878106f9f68b14ff4a48^ -- javacode.java
fatal: no such path javacode.java in 63995283ff201961a709878106f9f68b14ff4a48^
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git blame 63995283ff201961a709878106f9f68b14ff4a48^ -- java_code.java
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 1) // This is a Java file
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 2) 
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 3) public class HelloWorld {
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 4)    public static void main(String[] args) {
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 5)       System.out.println("Привет от Java!");
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 6)    }
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 7) }
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git log --oneline
6399528 (HEAD -> exercise9) Delete java code
37363ce Testing the emergency git-casting system
88f6e28 (upstream/exercise9) Adding bash, python, and java code examples
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, master) Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git bisect 6399528 43388fe
usage: git bisect [help|start|bad|good|new|old|terms|skip|next|reset|visualize|view|replay|log|run]
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git bisect start 6399528 43388feBisecting: 0 revisions left to test after this (roughly 1 step)
[37363ce5149cb06aa2bc1115b05c9f2e1e05c7fa] Testing the emergency git-casting system
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ cat hello.txt
Hello World!
This is a test of the emergency git-casting system.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git bisect bad
Bisecting: 0 revisions left to test after this (roughly 0 steps)
[88f6e2864bd0829c71654f1d19096f436a66ce07] Adding bash, python, and java code examples
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git bisect bad
88f6e2864bd0829c71654f1d19096f436a66ce07 is the first bad commit
commit 88f6e2864bd0829c71654f1d19096f436a66ce07
Author: Nina Zakharenko <nina@nnja.io>
Date:   Thu Oct 5 11:31:34 2017 -0700

    Adding bash, python, and java code examples

 bash_code.sh   | 3 +++
 java_code.java | 7 +++++++
 python_code.py | 4 ++++
 3 files changed, 14 insertions(+)
 create mode 100644 bash_code.sh
 create mode 100644 java_code.java
 create mode 100644 python_code.py
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git bisect good
88f6e2864bd0829c71654f1d19096f436a66ce07 was both good and bad
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git bisect reset
M	python_code.py
Previous HEAD position was 88f6e28 Adding bash, python, and java code examples
Switched to branch 'exercise9'
Your branch is ahead of 'upstream/exercise9' by 2 commits.
  (use "git push" to publish your local commits)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git status
On branch exercise9
Your branch is ahead of 'upstream/exercise9' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   python_code.py

no changes added to commit (use "git add" and/or "git commit -a")
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ echo python_code
python_code
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/courses/advanced-git-exercises$ git log --oneline
6399528 (HEAD -> exercise9) Delete java code
37363ce Testing the emergency git-casting system
88f6e28 (upstream/exercise9) Adding bash, python, and java code examples
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, master) Initial commit

```
