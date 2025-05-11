PS C:\PC1repo> git clone https://github.com/git1egyprogramozo/PC1test.git
Cloning into 'PC1test'...
warning: You appear to have cloned an empty repository.
PS C:\PC1repo> cd .\PC1test\
PS C:\PC1repo\PC1test> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\PC1repo\PC1test> Copy-Item -Path "C:\PC1repo\teszt3.txt" -Destination "C:\PC1repo\PC1test"
PS C:\PC1repo\PC1test> dir


    Directory: C:\PC1repo\PC1test


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         5/11/2025   7:42 PM              9 teszt3.txt


PS C:\PC1repo\PC1test> git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        teszt3.txt

nothing added to commit but untracked files present (use "git add" to track)
PS C:\PC1repo\PC1test> git add .
PS C:\PC1repo\PC1test> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   teszt3.txt

PS C:\PC1repo\PC1test> git commit -m "First commit.."
[main (root-commit) 482f09e] First commit..
 1 file changed, 1 insertion(+)
 create mode 100644 teszt3.txt
PS C:\PC1repo\PC1test> git status
On branch main
Your branch is based on 'origin/main', but the upstream is gone.
  (use "git branch --unset-upstream" to fixup)

nothing to commit, working tree clean
PS C:\PC1repo\PC1test> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 225 bytes | 56.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/git1egyprogramozo/PC1test.git
 * [new branch]      main -> main
PS C:\PC1repo\PC1test> dir


    Directory: C:\PC1repo\PC1test


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         5/11/2025   7:42 PM              9 teszt3.txt


PS C:\PC1repo\PC1test> Remove-Item teszt3.txt
PS C:\PC1repo\PC1test> dir
PS C:\PC1repo\PC1test> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    teszt3.txt

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\PC1repo\PC1test> git add .
PS C:\PC1repo\PC1test> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    teszt3.txt

PS C:\PC1repo\PC1test> git commit -m "del teszt3.txt"
[main 091c718] del teszt3.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 teszt3.txt
PS C:\PC1repo\PC1test> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (2/2), 198 bytes | 66.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/git1egyprogramozo/PC1test.git
   482f09e..091c718  main -> main
PS C:\PC1repo\PC1test>
