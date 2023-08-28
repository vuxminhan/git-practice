```Script started on 2023-08-28 16:01:47+07:00 [TERM="dump" TTY="/dev/pts/0" COLUMNS="80" LINES="24"]
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1$ mkdir -p project/s</OneDrive/lab/git-practice/ex1$ mkdir -p project/sa                         mple
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1$ cd project/sample
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          init    status
fatal: not a git repository (or any of the parent directories): .git
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: git branch -m <name>
Initialized empty Git repository in /home/alex/OneDrive/lab/git-practice/ex1/project/sample/.git/
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ tre</OneDrive/lab/git-practice/ex1/project/sample$ tree                          .git
.git
 branches
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
 info
  exclude
 objects
  info
  pack
 refs
     heads
     tags

9 directories, 17 files
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          cat-file -t              alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ gi  tou</OneDrive/lab/git-practice/ex1/project/sample$ touc                         h hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ ech</OneDrive/lab/git-practice/ex1/project/sample$ echo                          hello > t hello             ""h"e"l"l"o" "w"o"r"l"d"</OneDrive/lab/git-practice/ex1/project/sample$ echo "hello world" > hello.tx</ex1/project/sample$ echo "hello world" > hello.txt                         
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ cat</OneDrive/lab/git-practice/ex1/project/sample$ cat                          hello.txt
hello world
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          add hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          commit -m ""i"n"i"t"i"" " " " " I"n"i"t"i"a"l" "c"o"m"m"i"t"
[master (root-commit) 80dcc4e] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 hello.txt
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                           alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ gi  git</OneDrive/lab/git-practice/ex1/project/sample$ git                           alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ gi  tre</OneDrive/lab/git-practice/ex1/project/sample$ tree                          .git
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
          master
 objects
  3b
   18e512dba79e4c8300dd08aeb37f8e728b8dad
  68
   aba62e560c0ebc3396e8ae9335232cd93a3f60
  80
   dcc4efb38fac61669302b97f6a9f04572176dc
  info
  pack
 refs
     heads
      master
     tags

15 directories, 25 files
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          cat-file 3b18e51
usage: git cat-file (-t [--allow-unknown-type] | -s [--allow-unknown-type] | -e | -p | <type> | --textconv | --filters) [--path=<path>] <object>
   or: git cat-file (--batch[=<format>] | --batch-check[=<format>]) [--follow-symlinks] [--textconv | --filters]

<type> can be one of: blob, tree, commit, tag
    -t                    show object type
    -s                    show object size
    -e                    exit with zero when there's no error
    -p                    pretty-print object's content
    --textconv            for blob objects, run textconv on object's content
    --filters             for blob objects, run filters on object's content
    --path <blob>         use a specific path for --textconv/--filters
    --allow-unknown-type  allow -s and -t to work with broken/corrupt objects
    --buffer              buffer --batch output
    --batch[=<format>]    show info and content of objects fed from the standard input
    --batch-check[=<format>]
                          show info about objects fed from the standard input
    --follow-symlinks     follow in-tree symlinks (used with --batch or --batch-check)
    --batch-all-objects   show all objects with --batch or --batch-check
    --unordered           do not order --batch-all-objects output

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ <t-practice/ex1/project/sample$ git cat-file 3b18e51                      <t-practice/ex1/project/sample$ git cat-file<t-practice/ex1/project/sample$ git cat-file  3b18e51- 3b18e51t 3b18e51
blob
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          cat-file -t 68aba6
tree
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          cat-file -t </g" my_output | tr -dc '[[:print:]]\n' > new_output                                                               )?[mGK]       [([0-9]{1,2}(;[0-9]{1,2})                         at-file -t sed -r "s/\x1B                         /ex1/project/sample$ git  alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ gi  git</OneDrive/lab/git-practice/ex1/project/sample$ git                          cat-file -t 80dcc4e
commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                           alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ gi  cat</OneDrive/lab/git-practice/ex1/project/sample$ cat                          .git/HEAD
ref: refs/heads/master
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ CAT</OneDrive/lab/git-practice/ex1/project/sample$ CAT                           alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ CA  cat</OneDrive/lab/git-practice/ex1/project/sample$ cat                          .git/dcc4e     refs/heads/master
80dcc4efb38fac61669302b97f6a9f04572176dc
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          cat-file -p 80dcc4efb3
tree 68aba62e560c0ebc3396e8ae9335232cd93a3f60
author vuxminhan <11210261@st.neu.edu.vn> 1693213398 +0700
committer vuxminhan <11210261@st.neu.edu.vn> 1693213398 +0700

Initial commit
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          branch -b new
error: unknown switch `b'
usage: git branch [<options>] [-r | -a] [--merged] [--no-merged]
   or: git branch [<options>] [-l] [-f] <branch-name> [<start-point>]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
   or: git branch [<options>] [-r | -a] [--format]

Generic options
    -v, --verbose         show hash and subject, give twice for upstream branch
    -q, --quiet           suppress informational messages
    -t, --track           set up tracking mode (see git-pull(1))
    -u, --set-upstream-to <upstream>
                          change the upstream info
    --unset-upstream      unset the upstream info
    --color[=<when>]      use colored output
    -r, --remotes         act on remote-tracking branches
    --contains <commit>   print only branches that contain the commit
    --no-contains <commit>
                          print only branches that don't contain the commit
    --abbrev[=<n>]        use <n> digits to display object names

Specific git-branch actions:
    -a, --all             list both remote-tracking and local branches
    -d, --delete          delete fully merged branch
    -D                    delete branch (even if not merged)
    -m, --move            move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    -c, --copy            copy a branch and its reflog
    -C                    copy a branch, even if target exists
    -l, --list            list branch names
    --show-current        show current branch name
    --create-reflog       create the branch's reflog
    --edit-description    edit the description for the branch
    -f, --force           force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --column[=<style>]    list branches in columns
    --sort <key>          field name to sort on
    --points-at <object>  print only branches of the object
    -i, --ignore-case     sorting and filtering are case insensitive
    --format <format>     format to use for the output

alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ git</OneDrive/lab/git-practice/ex1/project/sample$ git                          branch        checkout -b new
Switched to a new branch 'new'
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ tre</OneDrive/lab/git-practice/ex1/project/sample$ tree                          e .git  /refs
.git/refs
 heads
  master
  new
 tags

2 directories, 2 files
alex@alex-Legion-5-15ACH6:~/OneDrive/lab/git-practice/ex1/project/sample$ exi</OneDrive/lab/git-practice/ex1/project/sample$ exit                         
exit

Script done on 2023-08-28 16:07:14+07:00 [COMMAND_EXIT_CODE="0"]
```
