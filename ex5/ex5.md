```
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice$ ls
advanced-git-exercises  ex1  ex2  ex3  ex4  README.md
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice$ cd advanced-git-exercises 
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git checkout exercise5
Branch 'exercise5' set up to track remote branch 'exercise5' from 'origin'.
Switched to a new branch 'exercise5'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log
commit ff91b70c7f23de6b168dc60478f270e8e3f992a8 (HEAD -> exercise5, origin/exercise5)
Merge: fec9e7b afa34a6
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:51:40 2017 -0700

    Merging in mundo branch

commit fec9e7b9f23a77bbc8e15603de0d7ea9152c7222
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:50:45 2017 -0700

    Changing Hello to Hola

commit 4582f72b8839b832aec19015bd0447ceac044899
Merge: 43388fe e348ebc
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:49:49 2017 -0700

    Merge branch 'exercise3' into exercise4

commit afa34a64f5711c79486465d6fa1c77a9a6109d84
Author: Nina Zakharenko <nina@nnja.io>
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ nano hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ cat hello.txt
[greeting] [noun]!
This is a test of the emergency git-casting system.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git mv hello.txt hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ ls
hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git add hello.template
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git commit
hint: Waiting for your editor to close the file... error: cannot run emacs: No such file or directory
error: unable to start editor 'emacs'
Please supply the message using either -m or -F option.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git config --global core.editor 'nano'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git commit
[exercise5 5ae380d] Replacing greeting with tokens for i18n
 1 file changed, 1 insertion(+), 1 deletion(-)
 rename hello.txt => hello.template (73%)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log
commit 5ae380dccebc1d28b1c260993ebc2e523b82e9f4 (HEAD -> exercise5)
Author: vuxminhan <11210261@st.neu.edu.vn>
Date:   Mon Aug 28 22:43:37 2023 +0700

    Replacing greeting with tokens for i18n
    
    Currently, hello.txt contains both Spanish and English.
    Let's replace Hola with a [greeting] token, and Mundo
    with a [noun] token. That way, we can localize hello.txt for
    any language!

commit ff91b70c7f23de6b168dc60478f270e8e3f992a8 (origin/exercise5)
Merge: fec9e7b afa34a6
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:51:40 2017 -0700

    Merging in mundo branch

commit fec9e7b9f23a77bbc8e15603de0d7ea9152c7222
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:50:45 2017 -0700

    Changing Hello to Hola
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ 
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --name-status --follow --oneline hello.template
5ae380d (HEAD -> exercise5) Replacing greeting with tokens for i18n
R073    hello.txt       hello.template
fec9e7b Changing Hello to Hola
M       hello.txt
afa34a6 Changing World to Mundo
M       hello.txt
e348ebc (tag: tag-with-anotation, tag: my-exercise3-tag, origin/exercise3, exercise3) Testing the emergency git-casting system
M       hello.txt
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master) Initial commit
A       hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --grep=i18n --author=nina --since=2.weeks
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --grep=i18n --author=nina 
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --grep=i18n
commit 5ae380dccebc1d28b1c260993ebc2e523b82e9f4 (HEAD -> exercise5)
Author: vuxminhan <11210261@st.neu.edu.vn>
Date:   Mon Aug 28 22:43:37 2023 +0700

    Replacing greeting with tokens for i18n
    
    Currently, hello.txt contains both Spanish and English.
    Let's replace Hola with a [greeting] token, and Mundo
    with a [noun] token. That way, we can localize hello.txt for
    any language!
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --grep=i18n --author=vuxminhan --since=2.weeks
commit 5ae380dccebc1d28b1c260993ebc2e523b82e9f4 (HEAD -> exercise5)
Author: vuxminhan <11210261@st.neu.edu.vn>
Date:   Mon Aug 28 22:43:37 2023 +0700

    Replacing greeting with tokens for i18n
    
    Currently, hello.txt contains both Spanish and English.
    Let's replace Hola with a [greeting] token, and Mundo
    with a [noun] token. That way, we can localize hello.txt for
    any language!
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --diff-filter=R --find-renames
commit 5ae380dccebc1d28b1c260993ebc2e523b82e9f4 (HEAD -> exercise5)
Author: vuxminhan <11210261@st.neu.edu.vn>
Date:   Mon Aug 28 22:43:37 2023 +0700

    Replacing greeting with tokens for i18n
    
    Currently, hello.txt contains both Spanish and English.
    Let's replace Hola with a [greeting] token, and Mundo
    with a [noun] token. That way, we can localize hello.txt for
    any language!
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log --diff-filter=M --oneline
fec9e7b Changing Hello to Hola
afa34a6 Changing World to Mundo
e348ebc (tag: tag-with-anotation, tag: my-exercise3-tag, origin/exercise3, exercise3) Testing the emergency git-casting system
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git log
commit 5ae380dccebc1d28b1c260993ebc2e523b82e9f4 (HEAD -> exercise5)
Author: vuxminhan <11210261@st.neu.edu.vn>
Date:   Mon Aug 28 22:43:37 2023 +0700

    Replacing greeting with tokens for i18n
    
    Currently, hello.txt contains both Spanish and English.
    Let's replace Hola with a [greeting] token, and Mundo
    with a [noun] token. That way, we can localize hello.txt for
    any language!

commit ff91b70c7f23de6b168dc60478f270e8e3f992a8 (origin/exercise5)
Merge: fec9e7b afa34a6
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:51:40 2017 -0700

    Merging in mundo branch

commit fec9e7b9f23a77bbc8e15603de0d7ea9152c7222
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:50:45 2017 -0700

    Changing Hello to Hola
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git show 5ae380
commit 5ae380dccebc1d28b1c260993ebc2e523b82e9f4 (HEAD -> exercise5)
Author: vuxminhan <11210261@st.neu.edu.vn>
Date:   Mon Aug 28 22:43:37 2023 +0700

    Replacing greeting with tokens for i18n
    
    Currently, hello.txt contains both Spanish and English.
    Let's replace Hola with a [greeting] token, and Mundo
    with a [noun] token. That way, we can localize hello.txt for
    any language!

diff --git a/hello.txt b/hello.template
similarity index 73%
rename from hello.txt
rename to hello.template
index 7018e35..a6c57ac 100644
--- a/hello.txt
+++ b/hello.template
@@ -1,2 +1,2 @@
-Hola Mundo!
+[greeting] [noun]!
 This is a test of the emergency git-casting system.
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git show 5ae380 --stat --oneline
5ae380d (HEAD -> exercise5) Replacing greeting with tokens for i18n
 hello.txt => hello.template | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git branch
  exercise2
  exercise3
  exercise4
* exercise5
  master
  mundo
  new
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git branch --merged master
  master
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ git branch --no-merged master
  exercise2
  exercise3
  exercise4
* exercise5
  mundo
  new
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/advanced-git-exercises$ 
```
