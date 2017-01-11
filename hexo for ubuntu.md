---
title: hexo for Ubuntu
date: 2016-11-09 15:00:00
tags: 
 - hexo
categories: 
 - hexo配置
---

## hexo for Ubuntu

[hexo官方安装手册](https://hexo.io/zh-cn/docs/)

[NVM工具安装](https://www.liquidweb.com/kb/how-to-install-nvm-node-version-manager-for-node-js-on-ubuntu-12-04-lts/)

**问题：**

 - 安装Hexo报错
npm install -g hexo-cli

解决办法：
替换成淘宝的源
npm install -g cnpm --registry=https://registry.npm.taobao.org
然后执行
cnpm install -g hexo-cli

 - 头像配置
使用png无法加载【使用的next的主题，themes/next/source/images/目录】


 - 部署配置
 ```bash
deploy: 
    type: git
    repo: https://www.github.com/xxx/xx.git
    branch: master
```

