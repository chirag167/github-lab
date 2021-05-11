1) The version of git is 2.21.1

2) When I issued the command git config --list:
OUTPUT:
credential.helper=osxkeychain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
user.name=chirag167
user.email=chiragrathi16798@gmail.com
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
core.ignorecase=true
core.precomposeunicode=true

3) It opens up the Git Manual and tells the functionality of the most commonly used commands. Some examples include cloning a repository, initializing a repository, adding files to the working tree etc. It also instructs about the usage of this command (git --help).

4) No committments are made yet and there are untracked files (which means that they are still in the index).
OUTPUT:
No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.md
	answers.md

nothing added to commit but untracked files present (use "git add" to track)

5) The README file has been pushed to the staging area. Now it is being tracked and the repository knows which file needs to be committed (as opposed to the answer in 4 where the repository did not know about any files). However, the committmment still needs to be made.
OUTPUT:
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	answers.md

6) Now both the files are in the staging area, ready to be committed.
OUTPUT:
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   README.md
	new file:   answers.md

7) OUTPUT:
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   answers.md

no changes added to commit (use "git add" and/or "git commit -a").

8) OUTPUT:
commit 575752bb1006d6f4fe2714d363443feb6cb3ee8a (HEAD -> master)
Author: chirag167 <chirag16798@gmail.com>
Date:   Tue May 11 09:44:39 2021 +0400

    Initial commit

9) OUTPUT: 

Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1.30 KiB | 1.30 MiB/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To https://github.com/chirag167/github-lab.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

10) No, changes made online were not reflected in my local directory.

11) OUTPUT:
To https://github.com/chirag167/github-lab.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/chirag167/github-lab.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

12) After giving the git pull command, the changes were made successfully. The online repository and my local working repository were in sync.

13) OUTPUT:
.		..		.git		.gitignore	README.md








