---
title: "Terminal Commands"
date: 2022-02-24T00:48:37-10:00
description: "Useful commands that I forget about."
type: post
tags: ["git", "terminal"]
---
### Git
* Absolute Path to Current Repository: `git rev-parse --show-toplevel`

### Finding IP

* Wireless IP Address: `ipconfig getifaddr en1`
* Ethernet IP Address: `ipconfig getifaddr en0`
* More straightforward way: `ifconfig | grep "inet " | grep -Fv 127.0.0.1 | awk '{print $2}' `


[Github Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)