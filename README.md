# Git
Everything about Git and practices.

## Table of Contents
1. [Introduction.](#introduction)
2. [Official references websites.](#references)
3. [Git Large File Storage (LFS).](#LFS)
4. [Check Git file size.](#gitsize)
5. [GitHub notes.](#github)

<a name="introduction"></a>
## 1. Introduction.
<img src="git.png" height="150"> 
Git is a distributed version-control system for tracking changes in source code during software development. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed,[9] data integrity, and support for distributed, non-linear workflows.

Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development. Its current maintainer since 2005 is Junio Hamano. As with most other distributed version-control systems, and unlike most client–server systems, every Git directory on every computer is a full-fledged repository with complete history and full version-tracking abilities, independent of network access or a central server. Git is free and open-source software distributed under the terms of the GNU General Public License version 2.

<a name="references"></a>
## 2. Official references websites. <br />
Git official website : https://git-scm.com <br />
GitHub official website : https://github.com <br />
Git Large File Storage (LFS) : https://git-lfs.github.com <br />

**_Git documentation_**
Configuring Git Large File Storage by GitHub : https://help.github.com/en/github/managing-large-files/configuring-git-large-file-storage <br />
REST API v3 by GitHub : https://developer.github.com/v3/ <br />

**_Git related articles_**
10 Useful du (Disk Usage) Commands to Find Disk Usage of Files and Directories : https://www.tecmint.com/check-linux-disk-usage-of-files-and-directories/ <br />
How To Run Your Own Git Server by Swapnil Bhartiya : https://www.linux.com/tutorials/how-run-your-own-git-server/ <br />
fallocate - preallocate or deallocate space to a file : http://man7.org/linux/man-pages/man1/fallocate.1.html <br />
How do you copy and paste into Git Bash : https://stackoverflow.com/questions/2304372/how-do-you-copy-and-paste-into-git-bash <br />

**_Git projects_**
VFS for Git : https://github.com/microsoft/VFSForGit<br />
Enterprise Config for Git : https://github.com/Autodesk/enterprise-config-for-git <br />

**_Git developers_**
Git was created by Linus Torvalds : https://github.com/torvalds <br />
Lars Schneider of GitHub : https://github.com/larsxschneider <br />
Chris Wanstrath, the founder of GitHub : https://github.com/defunkt <br />
Nat Friedman, Chief Executive Officer (CEO) of GitHub : https://github.com/nat <br />

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

<a name="gitsize"></a>
## 4. Check Git file size.
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

<a name="github"></a>
## 5. GitHub notes.
Clone the current GitHub remote repository contents into local machine.
```
$ git clone https://github.com/syakirharis25/Git.git
$ cd Git/
$ git remote -v
$ git status
```

GitHub markdown-cheatsheet by tchap : https://github.com/tchapi/markdown-cheatsheet/blob/master/README.md
