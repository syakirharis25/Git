# Git
Everything about Git and practices.

## Table of Contents
1. [Introduction.](#introduction)
2. [Official references websites.](#references)
3. [Git Large File Storage (LFS).](#LFS)
4. [GitHub notes.](#github)

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

Git was created by Linus Torvalds : https://github.com/torvalds <br />

<a name="LFS"></a>
## 3. Git Large File Storage (LFS).
Git Large File Storage (LFS) replaces large files such as audio samples, videos, datasets, and graphics with text pointers inside Git, while storing the file contents on a remote server like GitHub.com or GitHub Enterprise.
<br /><br />
"git large file storage" or git-lfs is a tool that helps with tracking large files inside a git repository while the file content is stored outside of git. The need for such functionality is necessitated by limitations in git performance which degrades as the size of the repository grows beyond a few megabytes. When storing files that are several hundred megabytes in size, git becomes prohibitively slow. git-lfs provides one method of addressing this problem.

To work with projects that use git-lfs, you need to download and install the git-lfs client on your workstation. The client can be downloaded from https://git-lfs.github.com, simply follow the instructions under "Getting Started" on the git-lfs site.

<a name="github"></a>
## 4. GitHub notes.
Clone the current GitHub remote repository contents into local machine.
```
$ git clone https://github.com/syakirharis25/Git.git
$ cd Git/
$ git remote -v
$ git status
```

GitHub markdown-cheatsheet by tchap : https://github.com/tchapi/markdown-cheatsheet/blob/master/README.md
