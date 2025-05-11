PS C:\PC1repo> git init
Initialized empty Git repository in C:/PC1repo/.git/
PS C:\PC1repo> git clone https://github.com/egyprogramozo/DOSCommands.git
Cloning into 'DOSCommands'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 10 (delta 4), reused 9 (delta 3), pack-reused 0 (from 0)
Receiving objects: 100% (10/10), 15.50 KiB | 1.72 MiB/s, done.
Resolving deltas: 100% (4/4), done.
PS C:\PC1repo> dir


    Directory: C:\PC1repo


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         5/11/2025   7:07 PM                DOSCommands


PS C:\PC1repo> cd .\DOSCommands\
PS C:\PC1repo\DOSCommands> dir


    Directory: C:\PC1repo\DOSCommands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         5/11/2025   7:07 PM             68 .gitattributes
-a----         5/11/2025   7:07 PM           9027 dosc000010.txt
-a----         5/11/2025   7:07 PM          35803 LICENSE


PS C:\PC1repo\DOSCommands> cd..
PS C:\PC1repo> Remove-Item -Path "C:\PC1repo\DOSCommands" -Recurse -Force
PS C:\PC1repo> dir
PS C:\PC1repo>
