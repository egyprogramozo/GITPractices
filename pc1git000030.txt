PS C:\PC1repo> git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\PC1repo> Set-Content -Path "teszt.txt" -Value "Valami"
PS C:\PC1repo> Add-Content -Path "teszt.txt" -Value "Új sor"
PS C:\PC1repo> Get-Content -Path "teszt.txt"
Valami
Új sor
PS C:\PC1repo> dir


    Directory: C:\PC1repo


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         5/11/2025   7:32 PM             16 teszt.txt


PS C:\PC1repo> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        teszt.txt

nothing added to commit but untracked files present (use "git add" to track)
PS C:\PC1repo> git add .\teszt.txt
PS C:\PC1repo> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   teszt.txt

PS C:\PC1repo> git commit -?
error: unknown switch `?'
usage: git commit [-a | --interactive | --patch] [-s] [-v] [-u[<mode>]] [--amend]
                  [--dry-run] [(-c | -C | --squash) <commit> | --fixup [(amend|reword):]<commit>]
                  [-F <file> | -m <msg>] [--reset-author] [--allow-empty]
                  [--allow-empty-message] [--no-verify] [-e] [--author=<author>]
                  [--date=<date>] [--cleanup=<mode>] [--[no-]status]
                  [-i | -o] [--pathspec-from-file=<file> [--pathspec-file-nul]]
                  [(--trailer <token>[(=|:)<value>])...] [-S[<keyid>]]
                  [--] [<pathspec>...]

    -q, --[no-]quiet      suppress summary after successful commit
    -v, --[no-]verbose    show diff in commit message template

Commit message options
    -F, --[no-]file <file>
                          read message from file
    --[no-]author <author>
                          override author for commit
    --[no-]date <date>    override date for commit
    -m, --[no-]message <message>
                          commit message
    -c, --[no-]reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --[no-]reuse-message <commit>
                          reuse message from specified commit
    --[no-]fixup [(amend|reword):]commit
                          use autosquash formatted message to fixup or amend/reword specified commit
    --[no-]squash <commit>
                          use autosquash formatted message to squash specified commit
    --[no-]reset-author   the commit is authored by me now (used with -C/-c/--amend)
    --trailer <trailer>   add custom trailer(s)
    -s, --[no-]signoff    add a Signed-off-by trailer
    -t, --[no-]template <file>
                          use specified template file
    -e, --[no-]edit       force edit of commit
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    --[no-]status         include status in commit message template
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit

Commit contents options
    -a, --[no-]all        commit all changed files
    -i, --[no-]include    add specified files to index for commit
    --[no-]interactive    interactively add files
    -p, --[no-]patch      interactively add changes
    -o, --[no-]only       commit only specified files
    -n, --no-verify       bypass pre-commit and commit-msg hooks
    --verify              opposite of --no-verify
    --[no-]dry-run        show what would be committed
    --[no-]short          show status concisely
    --[no-]branch         show branch information
    --[no-]ahead-behind   compute full ahead/behind values
    --[no-]porcelain      machine-readable output
    --[no-]long           show status in long format (default)
    -z, --[no-]null       terminate entries with NUL
    --[no-]amend          amend previous commit
    --no-post-rewrite     bypass post-rewrite hook
    --post-rewrite        opposite of --no-post-rewrite
    -u, --[no-]untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)
    --[no-]pathspec-from-file <file>
                          read pathspec from file
    --[no-]pathspec-file-nul
                          with --pathspec-from-file, pathspec elements are separated with NUL character

PS C:\PC1repo> git commit -m "This is my first commit."
[master (root-commit) 8fbe703] This is my first commit.
 1 file changed, 2 insertions(+)
 create mode 100644 teszt.txt
PS C:\PC1repo> git status
On branch master
nothing to commit, working tree clean
PS C:\PC1repo> Set-Content -Path "teszt2.txt" -Value "Valami2"
PS C:\PC1repo> Set-Content -Path "teszt3.txt" -Value "Valami3"
PS C:\PC1repo> dir


    Directory: C:\PC1repo


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         5/11/2025   7:32 PM             16 teszt.txt
-a----         5/11/2025   7:42 PM              9 teszt2.txt
-a----         5/11/2025   7:42 PM              9 teszt3.txt


PS C:\PC1repo> git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        teszt2.txt
        teszt3.txt

nothing added to commit but untracked files present (use "git add" to track)
PS C:\PC1repo> git add .
PS C:\PC1repo> git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   teszt2.txt
        new file:   teszt3.txt

PS C:\PC1repo> git commit -m "My second attempt."
[master 3693a3e] My second attempt.
 2 files changed, 2 insertions(+)
 create mode 100644 teszt2.txt
 create mode 100644 teszt3.txt
PS C:\PC1repo> git status
On branch master
nothing to commit, working tree clean
PS C:\PC1repo> Add-Content -Path "teszt2.txt" -Value "Új sor"
PS C:\PC1repo> git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   teszt2.txt

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\PC1repo> type "teszt2.txt"
Valami2
Új sor
PS C:\PC1repo> git add .
PS C:\PC1repo> git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   teszt2.txt

PS C:\PC1repo> git commit -m "My third commit."
[master 4d36426] My third commit.
 1 file changed, 1 insertion(+)
PS C:\PC1repo> git status
On branch master
nothing to commit, working tree clean
PS C:\PC1repo>
