# My Get Notes

## Generate SSH Key on Local Machine

```bash
kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub
$ ssh-keygen -t rsa
``` 

Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/kella/.ssh/id_rsa):
Created directory '/c/Users/kella/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/kella/.ssh/id_rsa.
Your public key has been saved in /c/Users/kella/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:DD87L4LNEaTKgsRVk4lFs6xKwrPUPiikNsYgh8b0Y2A kella@DESKTOP-D0N6VOQ
The key's randomart image is:
+---[RSA 3072]----+
kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub$ ssh-keygen -t rsaGenerating public/private rsa key pair.
Enter file in which to save the key (/c/Users/kella/.ssh/id_rsa):
Created directory '/c/Users/kella/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/kella/.ssh/id_rsa.
Your public key has been saved in /c/Users/kella/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:DD87L4LNEaTKgsRVk4lFs6xKwrPUPiikNsYgh8b0Y2A kella@DESKTOP-D0N6VOQ
The key's randomart image is:
+---[RSA 3072]----+
|    =*o          |
|   o.o=          |
|.E.  =.          |
|=++ o .+         |
|BX.B   .S        |
|&.X . .  o       |
|oX o + .o        |
|+ . o + .o       |
|       . ..      |
+----[SHA256]-----+

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub
$ more /c/Users/kella/.ssh/id_rsa.pub
bash: more: command not found

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub
$ less /c/Users/kella/.ssh/id_rsa.pub

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub
$ git clone git@github.com:KscheiberAI/best-repo-ever.git
Cloning into 'best-repo-ever'...
The authenticity of host 'github.com (192.30.253.113)' can't be established.
RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub
$ git status
fatal: not a git repository (or any of the parent directories): .git

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub
$ ls
best-repo-ever  trainingGitHubWS.code-workspace

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub
$ cd best-repo-ever

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git commit -am "first commit"
[master 4b44785] first commit
 1 file changed, 3 insertions(+), 1 deletion(-)

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git log
commit 4b44785f3be76748c2e820921610ffac5bcf1e75 (HEAD -> master)
Author: Kellan Scheiber <kellan.scheiber@atrium.ai>
Date:   Mon Jun 24 10:12:01 2019 -0400

    first commit

commit ae5379d205ae982368f8ffd083c8e98deff4b83e (origin/master, origin/HEAD)
Author: KscheiberAI <52077417+KscheiberAI@users.noreply.github.com>
Date:   Mon Jun 24 09:56:30 2019 -0400

    Initial commit

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git remote
origin

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git remote -a
error: unknown switch `a'
usage: git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <name> <url>
   or: git remote rename <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)...]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

    -v, --verbose         be verbose; must be placed before a subcommand


kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git remote -v
origin  git@github.com:KscheiberAI/best-repo-ever.git (fetch)
origin  git@github.com:KscheiberAI/best-repo-ever.git (push)

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$ git push origin master:master
Warning: Permanently added the RSA host key for IP address '192.30.253.112' to the list of known hosts.
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 274 bytes | 274.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To github.com:KscheiberAI/best-repo-ever.git
   ae5379d..4b44785  master -> master

kella@DESKTOP-D0N6VOQ MINGW64 ~/Documents/TrainingGitHub/best-repo-ever (master)
$