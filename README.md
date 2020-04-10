# Git
Everything about Git and practices.

## Table of Contents
1. [Introduction.](#introduction)
2. [Official references websites.](#references)
3. [Git Large File Storage (LFS).](#LFS)
4. [Using git command in Command Prompt.](#git) 
5. [Copy from browser and paste in Git Bash keyboard shortcut.](#copypaste)
6. [Check Git file size.](#gitsize)
7. [Git reference error.](#gitreference)
8. [Does not have a commit checked out error.](#checkedout)
9. [Git developers.](#developers)
10. [GitHub notes.](#github)
11. [GitHub repository calculation.](#calculation)

<a name="introduction"></a>
## 1. Introduction.
<img src="git.png" height="150"> 
Git is a distributed version-control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows.
<br /><br />
Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development. Its current maintainer since 2005 is Junio Hamano. As with most other distributed version-control systems, and unlike most client–server systems, every Git directory on every computer is a full-fledged repository with complete history and full version-tracking abilities, independent of network access or a central server. Git is free and open-source software distributed under the terms of the GNU General Public License version 2.

<a name="references"></a>
## 2. Official references websites. <br />
Git official website : https://git-scm.com <br />
GitHub official website : https://github.com <br />
GitHub Support official website : https://support.github.com <br />

**_Git related technologies_** <br />
Git Large File Storage (LFS) : https://git-lfs.github.com <br />
Git for Windows : https://gitforwindows.org <br />

**_Git related projects_** <br />
BFG Repo-Cleaner : https://rtyley.github.io/bfg-repo-cleaner/ <br /> 

**_Git questions and answers_** <br />
Stack Overflow questions and answers website : https://stackoverflow.com <br />

**_Git by GitHub_** <br />
GitHub official status on twitter : https://twitter.com/githubstatus <br />

**_Git documentation by GitHub_** <br />
Configuring Git Large File Storage by GitHub : https://help.github.com/en/github/managing-large-files/configuring-git-large-file-storage <br />
REST API v3 by GitHub : https://developer.github.com/v3/ <br />
Changing a commit message by GitHub : https://help.github.com/en/github/committing-changes-to-your-project/changing-a-commit-message <br />

**_Git documentation by Atlassian_** <br />
Git Merge by Atlassian : https://www.atlassian.com/git/tutorials/using-branches/git-merge <br />

**_Git questions and answers by Stack Overflow_** <br />
Git refusing to merge unrelated histories on rebase by Stack Overflow : https://stackoverflow.com/questions/37937984/git-refusing-to-merge-unrelated-histories-on-rebase <br />
How do you copy and paste into Git Bash by Stack Overflow : https://stackoverflow.com/questions/2304372/how-do-you-copy-and-paste-into-git-bash <br />
Why does git say “Pull is not possible because you have unmerged files”? by Stack Overflow : https://stackoverflow.com/questions/26376832/why-does-git-say-pull-is-not-possible-because-you-have-unmerged-files <br />
'git' is not recognized as an internal or external command by Stack Overflow : https://stackoverflow.com/questions/4492979/git-is-not-recognized-as-an-internal-or-external-command <br />
git pull fails “unable to resolve reference” “unable to update local ref” by Stack Overflow : https://stackoverflow.com/questions/2998832/git-pull-fails-unable-to-resolve-reference-unable-to-update-local-ref <br />
Git unable to resolve references when pushing by Stack Overflow : https://stackoverflow.com/questions/23749886/git-unable-to-resolve-references-when-pushing/23847239 <br />
How to fix: error: '<filename>' does not have a commit checked out fatal: adding files failed when inputting “git add .” in command prompt by Stack Overflow : https://stackoverflow.com/questions/56873278/how-to-fix-error-filename-does-not-have-a-commit-checked-out-fatal-adding <br />
Git : Merging Issues with Git by Stack Overflow : https://stackoverflow.com/questions/11527069/git-merging-issues-with-git/22990740<br />
You have not concluded your merge (MERGE_HEAD exists) by Stack Overflow : https://stackoverflow.com/questions/11646107/you-have-not-concluded-your-merge-merge-head-exists <br />

**_Git related articles_** <br />
10 Useful du (Disk Usage) Commands to Find Disk Usage of Files and Directories : https://www.tecmint.com/check-linux-disk-usage-of-files-and-directories/ <br />
How To Run Your Own Git Server by Swapnil Bhartiya : https://www.linux.com/tutorials/how-run-your-own-git-server/ <br />
fallocate - preallocate or deallocate space to a file : http://man7.org/linux/man-pages/man1/fallocate.1.html <br />
Changing a remote's URL by GitHub : https://help.github.com/en/github/using-git/changing-a-remotes-url <br />
How to delete multiples files in Github by GitHub Community Forum : https://github.community/t5/How-to-use-Git-and-GitHub/How-to-delete-multiples-files-in-Github/td-p/4623 <br />
How to Push an Existing Project to GitHub by Nicholas Cerminara : https://scotch.io/tutorials/how-to-push-an-existing-project-to-github <br />

**_Git projects_** <br />
VFS for Git : https://github.com/microsoft/VFSForGit<br />
Enterprise Config for Git : https://github.com/Autodesk/enterprise-config-for-git <br />

<a name="LFS"></a>
## 3. Git Large File Storage (LFS).
Git Large File Storage (LFS) replaces large files such as audio samples, videos, datasets, and graphics with text pointers inside Git, while storing the file contents on a remote server like GitHub.com or GitHub Enterprise.
<br /><br />
"git large file storage" or git-lfs is a tool that helps with tracking large files inside a git repository while the file content is stored outside of git. The need for such functionality is necessitated by limitations in git performance which degrades as the size of the repository grows beyond a few megabytes. When storing files that are several hundred megabytes in size, git becomes prohibitively slow. git-lfs provides one method of addressing this problem.

To work with projects that use git-lfs, you need to download and install the git-lfs client on your workstation. The client can be downloaded from https://git-lfs.github.com, simply follow the instructions under "Getting Started" on the git-lfs site.

To install git-lfs on Git Bash, simply do this command.
```
$ git lfs install
```
<a name="introduction"></a>
## 4. Using git command in Command Prompt.
To use code command in Command Prompt, you need to add `C:\Program Files\Git\bin\` and `C:\Program Files\Git\cmd\` into the windows environment PATH, follow this instructions. On the right hand side of **[ ⊞ ]**, type `edit environment` and then **[ Mouse Left Click ]** the shown text `edit environment variables for your account`, **Environment Variables** menu will appear, press **[ P ]**, make sure the `Path` is highlighted on the screen, then press **[ Tab ]**, **[ E ]**,**[ Tab ]**, **[ N ]**, and then type `C:\Program Files\Git\bin\`, then press **[ Enter ]**,**[ Tab ]**, **[ N ]**, **[ Enter ]**,and then type `C:\Program Files\Git\cmd\` **[ Enter ]**, **[ Enter ]**, **[ Enter ]**,**[ Tab ]**,**[ Tab ]**,**[ Tab ]**,**[ Enter ]**.

Press **[ ⊞ ]** + **[ R ]**, then press **[ C ]**, **[ M ]**, **[ D ]**, **[ Ctrl ]** + **[ Shift ]** + **[ Enter ]**, **[ ← ]**, **[ Enter ]**. Then type this commands to test whether git is running or not on the Command Prompt.
```
> git --version
```

<a name="copypaste"></a>
## 5. Copy from browser and paste in Git Bash keyboard shortcut.
To copy from browser, press **[ Ctrl ]** + **[ C ]** on your keyboard.
To paste into Git Bash, press **[ Shift ]** + **[ Insert ]** on your keyboard.

<a name="gitsize"></a>
## 6. Check Git file size.
To check Git file size do the following commands.
```
du -sh .git/
```

It will then show the message.
```
Updated git hooks.
Git LFS initialized.
```

To see what is inside git hooks, do this commands
```
$ ls -latr .git/hooks/
```

<a name="gitreference"></a>
## 7. Git reference error.
If there is a message shown on the screen saying that,
```
error: cannot lock ref 'refs/remotes/origin/master': unable to resolve reference 'refs/remotes/origin/master': reference broken
 ! [new branch]      master     -> origin/master  (unable to update local ref)
```

Then you must remove the broken reference, fetch back the Git reference address, and test again to pull the contents from GitHub repository to see whether it works or not.
```
$ rm .git/refs/remotes/origin/master
$ git fetch --prune
$ git pull origin master
```

<a name="checkedout"></a>
## 8. Does not have a commit checked out error.

If there is an error stated that `error: 'folder-name/' does not have a commit checked out`, then  you need to remove recursively the `.git/` folder in order to be able to add the related files into the remote Git repository.

```
$ cd folder-name
$ ls -a
$ rm - r.git/
$ cd ..
$ git status
$ git add .
$ git status
```

<a name="developers"></a>
## 9. Git developers.
Git was created by Linus Torvalds : https://github.com/torvalds <br />
Chris Wanstrath, the founder of GitHub : https://github.com/defunkt <br />
Kelvin Yap : https://twitter.com/kelvinyap <br />
Lars Schneider of GitHub : https://github.com/larsxschneider <br />
Nat Friedman, Chief Executive Officer (CEO) of GitHub : https://github.com/nat <br />
Nicholas Cerminara : https://twitter.com/gazelleeatslion, https://github.com/whatnickcodes <br />

<a name="github"></a>
## 10. GitHub notes.
Clone the current GitHub remote repository contents into local machine.
```
$ git clone https://github.com/syakirharis25/Git.git
$ cd Git/
$ git remote -v
$ git status
```

GitHub markdown-cheatsheet by tchap : https://github.com/tchapi/markdown-cheatsheet/blob/master/README.md

<a name="calculation"></a>
## 11. GitHub repository calculation.
```
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
Markdown                         1              0              0              2
-------------------------------------------------------------------------------
```
Refer to : https://github.com/syakirharis25/cloc
