---
title: SSH key生成及配置
date: 2016-11-10 11:30:00
tags: 
 - SSH key
catagories: SSH key
---

## SSH key检测
列出.ssh目录中的文件
```bash
ls -al ~/.ssh
```

## SSH key生成
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

## 添加SSH key到ssh-agent
```bash
ssh-add ~/.ssh/id_rsa
```

> - 从ssh-agent中删除秘钥 
> ```bash ssh-add -d ~/.ssh/id_xxx.pub ```
> - 查看ssh-agent中秘钥 
> ```bash ssh-add -l ```


## 添加SSH key到github账户
- 拷贝SSH key到剪贴板
```bash
pbcopy < ~/.ssh/id_rsa.pub
```

- 添加到github账户的SSH key中


## 测试SSH连接
```bash
ssh -T git@github.com
```

## 多个SSH配置
- 在`~/.ssh`目录下新建`config`文件
- 内容如下
```bash
# github
  Host github.com
  HostName github.com
  User name1
  IdentityFile ~/.ssh/id_rsa

# oschina
  Host oschina
  HostName oschina.com
  User name2
  IdentityFile ~/.ssh/oschina_id_rsa
```


----------
注： 更换电脑的情况下，ssh key(包括 id_rsa, id_rsa.pub两个文件)文件可以拷贝到其他电脑继续使用，不需要每台电脑生成一下，并改变两个文件的权限
```bash
chmod 600 id_rsa
chmod 644 id_rsa.pub
```
添加到ssh-agent，如果多个ssh key则配置下config文件

----------