---
title: pod使用
date: 2016-11-03 16:15:12
tags:
---

### Cocoapods安装
```bash
gem sources --remove https://rubygems.org/
gem sources -a https://ruby.taobao.org/ 
sudo gem install cocoapods
```

### Cocoapods升级
```bash
sudo gem update --system
sudo gem install cocoapods
pod setup
pod --version
```

### Cocoapods删除
```bash
sudo gem uninstall cocoapods
```

### 安装指导版本
```bash
sudo gem install cocoapods -v 1.0.1
```

### 错误处理
* `"not permitted"` 解决办法
```bash
sudo gem install -n /usr/local/bin cocoapods
```
