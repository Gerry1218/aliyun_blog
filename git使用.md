---
title: git使用
date: 2016-11-03 15:55:12
tags:
---

## Git使用

### 列出远程分支
```bash
git remote -v
```

### 更换远程仓库地址
断开之前远程仓库的关联 `origin` 是原仓库名
```bash
git remote rm orign
```

关联新的远程仓库
```bash
git remote add origin git@github.com:Gerry1218/aliyun_blog.git 
```

### 关联远程仓库到本地
初始化本地仓库
```bash
git init 
```

关联本地仓库和远程仓库
```bash
git remote add origin git@github.com:Gerry1218/aliyun_blog.git 
```

添加本地文件
```bash
git add .
```

提交本地文件
```bash
git commit -m "提交介绍"
```

推送到远程仓库, 第一次push的时候需添加`-u`参数，关联远程仓库
`origin` 远程仓库的名字
`master` 远程仓库的分支
```bash
git push -u origin master
```


