PS C:\PC2repo> git clone https://github.com/git1egyprogramozo/PC1test.git
Cloning into 'PC1test'...
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 5 (delta 0), reused 5 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (5/5), done.
PS C:\PC2repo> dir


    Directory: C:\PC2repo


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         5/11/2025   9:24 PM                PC1test


PS C:\PC2repo> cd .\PC1test\
PS C:\PC2repo\PC1test> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
PS C:\PC2repo\PC1test> @"
>> Ez egy első sor.
>> Ez egy második sor.
>> Ez egy harmadik sor.
>> "@ | Out-File -FilePath "C:\PC2repo\PC1test\szoveg.txt"
PS C:\PC2repo\PC1test> type .\szoveg.txt
Ez egy első sor.
Ez egy második sor.
Ez egy harmadik sor.
PS C:\PC2repo\PC1test> git add .
PS C:\PC2repo\PC1test> git commit -m "PC2 commit-ol PC1 repo-ba"
[main 9e07539] PC2 commit-ol PC1 repo-ba
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 szoveg.txt
PS C:\PC2repo\PC1test> git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\PC2repo\PC1test> git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 318 bytes | 63.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/git1egyprogramozo/PC1test.git
   091c718..9e07539  main -> main
PS C:\PC2repo\PC1test>
