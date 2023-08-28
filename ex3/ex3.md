```Script started on 2023-08-28 16:34:23+07:00 [TERM="dump" TTY="/dev/pts/0" COLUMNS="80" LINES="24"]
</OneDrive/lab/git-practice/advanced-git-exercises$ cat     git     tree .git
.git
 branches
 COMMIT_EDITMSG
 config
 description
 HEAD
 hooks
  applypatch-msg.sample
  commit-msg.sample
  fsmonitor-watchman.sample
  post-update.sample
  pre-applypatch.sample
  pre-commit.sample
  pre-merge-commit.sample
  prepare-commit-msg.sample
  pre-push.sample
  pre-rebase.sample
  pre-receive.sample
  push-to-checkout.sample
  update.sample
 index
 info
  exclude
 logs
  HEAD
  refs
      heads
       exercise2
       exercise3
       master
      remotes
       origin
           HEAD
      stash
 objects
  34
   2c8383e7ea8f5bff929307d3cdbf5ce6d0a2c5
  49
   fcc02d882a5d86163881c570c81a72cdc3bb0b
  4a
   452461abad471a2817b7d9f94d698be07d619f
  57
   61bf4c59dc5aef55c49b1c022688474c129eb6
  dd
   c5e4e795651d7e59e10c31da19dbd32e0f3845
  info
  pack
      pack-c7b232161b369af2e3813cdad8c019deb5ec59ac.idx
      pack-c7b232161b369af2e3813cdad8c019deb5ec59ac.pack
 ORIG_HEAD
 packed-refs
 refs
     heads
      exercise2
      exercise3
      master
     remotes
      origin
          HEAD
     stash
     tags

21 directories, 39 files
</OneDrive/lab/git-practice/advanced-git-exercises$ cat .git/HEAD
ref: refs/heads/exercise3
</OneDrive/lab/git-practice/advanced-git-exercises$ git show-refs heads     --heads
git: 'show-refs' is not a git command. See 'git --help'.

The most similar command is
show-ref
</OneDrive/lab/git-practice/advanced-git-exercises$ git show-refs --heads --heads 
342c8383e7ea8f5bff929307d3cdbf5ce6d0a2c5 refs/heads/exercise2
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/heads/exercise3
43388fee19744e8893467331d7853a6475a227b8 refs/heads/master
</OneDrive/lab/git-practice/advanced-git-exercises$ git cat-file -p <ed-git-exercises$ git cat-file -p refs/heads/master                
tree 581caa0fe56cf01dc028cc0b089d364993e046b6
author Nina Zakharenko <nina@nnja.io> 1507168309 -0700
committer Nina Zakharenko <nina@nnja.io> 1507168309 -0700

Initial commit
</OneDrive/lab/git-practice/advanced-git-exercises$ git cat       git cat       git show        giit    t cat-file -p </g" my_output | tr -dc '[[:print:]]\n' > new_output                                                                   2})?)?[mGK]           x1B\[([0-9]{1,2}(;[0-9]{1                         it cat-file -p sed -r "s/                         /advanced-git-exercises$ git cat-file -p refs/heads/exercise3
tree cbcdf5dda7853d595fe0b1942cb0d1d72eb910f3
parent 43388fee19744e8893467331d7853a6475a227b8
author Nina Zakharenko <nina@nnja.io> 1507168872 -0700
committer Nina Zakharenko <nina@nnja.io> 1507168872 -0700

Testing the emergency git-casting system
</OneDrive/lab/git-practice/advanced-git-exercises$ git tag my-exercise3-tag
</OneDrive/lab/git-practice/advanced-git-exercises$ git show-ref --tags
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/tags/my-exercise3-tag
</OneDrive/lab/git-practice/advanced-git-exercises$ git a tag --points-at e348
WARNING: terminal is not fully functional
Press RETURN to continue 
my-exercise3-tag
</OneDrive/lab/git-practice/advanced-git-exercises$ git at  tag -a ""t"a"g" "w"i"t"h" "a"n"o"t"</advanced-git-exercises$ git tag -a "tag with anota"                         t"i"o"n"</advanced-git-exercises$ git tag -a "tag with anotation" -m ""T"h"i"s" "i"s" "a"n" "a"n"n"o"<it tag -a "tag with anotation" -m "This is an annot"                         a"t"e"d" "t"a"g" "f"o"r" "e"x"3"<it tag -a "tag with anotation" -m "This is an annotated tag for ex3"
fatal: 'tag with anotation' is not a valid tag name.
</OneDrive/lab/git-practice/advanced-git-exercises$ <th anotation" -m "This is an annotated tag for ex3"it tag -a "tag with anotation" -m "This is an annotated tag for ex3"<it tag -a "tag w/advanced-git-exercises$ git tag -a "tag with anotation" -m "This is an annot></advanced-git-exercises$ </advanced-git-exercises$ g</advanced-git-exercises$ gi</advanced-git-exercises$ git</advanced-git-exercises$ git </advanced-git-exercises$ git t</advanced-git-exercises$ git ta</advanced-git-exercises$ git tag</advanced-git-exercises$ git tag </advanced-git-exercises$ git tag -</advanced-git-exercises$ git tag -a</advanced-git-exercises$ git tag -a </advanced-git-exercises$ git tag -a "</advanced-git-exercises$ git tag -a "t</advanced-git-exercises$ git tag -a "ta</advanced-git-exercises$ git tag -a "tag</advanced-git-exercises$ git tag -a "tag with anotation" -m "This is an annota>-with anotation" -m "This is an annot></advanced-git-exercises$ git tag -a "tag-w</advanced-git-exercises$ git tag -a "tag-wi</advanced-git-exercises$ git tag -a "tag-wit</advanced-git-exercises$ git tag -a "tag-with</advanced-git-exercises$ git tag -a "tag-with anotation" -m "This is an annota>-anotation" -m "This is an annot>
</OneDrive/lab/git-practice/advanced-git-exercises$ g git show-ref t --tags
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/tags/my-exercise3-tag
f7944af2a464a912dcc04c86be8f19c98a1213fd refs/tags/tag-with-anotation
</OneDrive/lab/git-practice/advanced-git-exercises$ git show <advanced-git-exercises$ git show tag-with-anotation         
WARNING: terminal is not fully functional
Press RETURN to continue 
tag tag-with-anotation
Tagger: vuxminhan <11210261@st.neu.edu.vn>
Date:   Mon Aug 28 16:40:02 2023 +0700

This is an annotated tag for ex3

commit e348ebc1187cb3b4066b1e9432a614b464bf9d07 (HEAD -> exercise3, tag: tag-wit
h-anotation, tag: my-exercise3-tag, origin/exercise3)
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:01:12 2017 -0700

    Testing the emergency git-casting system

diff --git a/hello.txt b/hello.txt
index 980a0d5..b31a35b 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1 +1,2 @@
 Hello World!
+This is a test of the emergency git-casting system.
</OneDrive/lab/git-practice/advanced-git-exercises$ git log
WARNING: terminal is not fully functional
Press RETURN to continue 
commit e348ebc1187cb3b4066b1e9432a614b464bf9d07 (HEAD -> exercise3, tag: tag-wit
h-anotation, tag: my-exercise3-tag, origin/exercise3)
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:01:12 2017 -0700

    Testing the emergency git-casting system

commit 43388fee19744e8893467331d7853a6475a227b8 (origin/master, origin/exercise7
, origin/exercise4, origin/exercise2, origin/HEAD, master)
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 18:51:49 2017 -0700

    Initial commit
</OneDrive/lab/git-practice/advanced-git-exercises$ git checout     kout e348ebc1
Note: switching to 'e348ebc1'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at e348ebc Testing the emergency git-casting system
</OneDrive/lab/git-practice/advanced-git-exercises$ touch test  .txt
</OneDrive/lab/git-practice/advanced-git-exercises$ echo ""T"i"s"" " h"i"s" "i"s" "a" "d"" t"e"s"t" "f"i"l"e"</advanced-git-exercises$ echo "This is a test file "                         " </advanced-git-exercises$ echo "This is a test file" > test.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git add test.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git commit -m ""d"a"n"g"l"e" "c"o"m"</advanced-git-exercises$ git commit -m "dangle comm"                         i"t"</advanced-git-exercises$ git commit -m "dangle commit"
[detached HEAD 10f33ce] dangle commit
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt
</OneDrive/lab/git-practice/advanced-git-exercises$ git log --oneline
WARNING: terminal is not fully functional
Press RETURN to continue 
10f33ce (HEAD) dangle commit
e348ebc (tag: tag-with-anotation, tag: my-exercise3-tag, origin/exercise3, exerc
ise3) Testing the emergency git-casting system
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, or
igin/HEAD, master) Initial commit
</OneDrive/lab/git-practice/advanced-git-exercises$ git checout   kout        status
HEAD detached from e348ebc
Untracked files:
  (use "git add <file>..." to include in what will be committed)
my_output

nothing added to commit but untracked files present (use "git add" to track)
</OneDrive/lab/git-practice/advanced-git-exercises$ git checou  kout exerceise     cise3
Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  10f33ce dangle commit

If you want to keep it by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> 10f33ce

Switched to branch 'exercise3'
Your branch is up to date with 'origin/exercise3'.
</OneDrive/lab/git-practice/advanced-git-exercises$ git checout       branch dangling        new   new 10f33ce
</OneDrive/lab/git-practice/advanced-git-exercises$ git show-reg fs 
git: 'show-refs' is not a git command. See 'git --help'.

The most similar command is
show-ref
</OneDrive/lab/git-practice/advanced-git-exercises$ git show-refs   
342c8383e7ea8f5bff929307d3cdbf5ce6d0a2c5 refs/heads/exercise2
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/heads/exercise3
43388fee19744e8893467331d7853a6475a227b8 refs/heads/master
10f33cef7addcc097a3f280bb4dfddb568d38521 refs/heads/new
43388fee19744e8893467331d7853a6475a227b8 refs/remotes/origin/HEAD
a198ae0f1cd37126e49408a17112a81cb4c42776 refs/remotes/origin/exercise10
43388fee19744e8893467331d7853a6475a227b8 refs/remotes/origin/exercise2
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/remotes/origin/exercise3
43388fee19744e8893467331d7853a6475a227b8 refs/remotes/origin/exercise4
ff91b70c7f23de6b168dc60478f270e8e3f992a8 refs/remotes/origin/exercise5
4b2b90ec4f526139ca9c81e22174ebf5b9c56b52 refs/remotes/origin/exercise6
43388fee19744e8893467331d7853a6475a227b8 refs/remotes/origin/exercise7
88f6e2864bd0829c71654f1d19096f436a66ce07 refs/remotes/origin/exercise9
43388fee19744e8893467331d7853a6475a227b8 refs/remotes/origin/master
ddc5e4e795651d7e59e10c31da19dbd32e0f3845 refs/stash
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/tags/my-exercise3-tag
f7944af2a464a912dcc04c86be8f19c98a1213fd refs/tags/tag-with-anotation
</OneDrive/lab/git-practice/advanced-git-exercises$ exit
exit

Script done on 2023-08-28 16:44:48+07:00 [COMMAND_EXIT_CODE="0"]
```
