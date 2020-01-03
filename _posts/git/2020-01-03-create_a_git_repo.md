---
layout: post
title: "Create git project"
subtitle: "Create and keep track your local project through git"
author: "Jack Pan"
header-img:   "img/git/git_logo.png"
header-mask:  0.5
tags:
  - git
  - github
---


## Create a git repo 

### Purpose

create a local git repo/ or use existed repo, and link it to remote source(like github)



### You will learn

1. How to create a local git repo
2. How to link local repo to remote repo
3. How to work with git, like branch, push file, etc.



### Lets go

#### prepare remote repo

I use github, so I get the github repo url:

![image-gitinit](/img/git/gitinit.png)

```
// create file
echo "# gitusagedemo" >> README.md
// init local git repo
git init
// make git track this file
git add README.md
// put this file to commit area
git commit -m "first commit"
// link local and remote repo
git remote add origin https://github.com/panq-jack/gitusagedemo.git
// push and track local file
git push -u origin master
```



#### link existed repo to remote

If you already have local repo, and wanna track it with remote one.

```
git remote add origin https://github.com/panq-jack/gitusagedemo.git
git push -u origin master
```

#### change repo track

If your  existed local repo already link to a remote repo, and wanna change it to another one.

```
git remote remove origin # 删掉原来git源
git remote add origin https://github.com/panq-jack/gitusagedemo.git
git push -u origin master
```



#### create a branch and work on it

```
// create and switch to another branch
git checkout -b feature/one
// create a local file
echo "# new branch: feature/one" >> desc.txt
git add desc.txt
git commit -m 'add desc file'
// push local branch to remote
git push -u origin feature/one
```



#### One more tip

check the track relationship b/w local and remote:

```
git branch -vv
```

console:

```
* feature/one 60b8d63 [origin/feature/one] add desc file
  master      ae0a6fa [origin/master] first commit
```







### What you learned

```
git init     # init local git repo
git remote add origin [YOUR NEW .GIT URL] # 将新源地址写入本地版本库配置文件
git checkout -b [branch_name] #create and switch to new branch
git push -u origin [branch_name] #push local branch to remote, and link them.
```




