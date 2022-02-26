---
title: "Terminal Commands"
date: 2022-02-24T00:48:37-10:00
description: "Useful commands that I forget about."
type: post
tags: ["git", "terminal"]
---
### Git
* Absolute Path to Current Repository: `git rev-parse --show-toplevel`
* Uninitialize git: `rm -rf .git`
* Reset remote url: `git remote set-url origin git@github.com:Laweeza/repo-name.git`
* Delete file: `git rm <file name>`
* Remove directory from git but not local: `git rm -r --cached myFolder`
* Move or rename a file: `git mv <options>…​ <args>…​` ([docs](https://git-scm.com/docs/git-mv))
* Rename a branch while pointed to any branch: `git branch -m <oldname> <newname>`
* Rename current branch: `git branch -m <newname>`
* Push to local branch and reset upstream branch: `git push origin -u <newname>`
* Delete the remote branch: `git push origin --delete <oldname>`

### Adding Aliases
* ```git config --global alias.rename 'branch -m'``` ([docs](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases))


### Finding IP Idress for VM

* Wireless IP Address: `ipconfig getifaddr en1`
* Ethernet IP Address: `ipconfig getifaddr en0`
* More straightforward way: `ifconfig | grep "inet " | grep -Fv 127.0.0.1 | awk '{print $2}' `


[Github Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)