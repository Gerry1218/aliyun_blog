---
title:  Next for hexo统计
date: 2016-11-10 13:00:00
tags: 
 - hexo
 - next
 - next 统计
catagories: hexo
---

## Next主题中添加文章统计
- 注册登录Leancloud
`控制台` -> `创建应用`  ->  `应用数据配置界面` ->  `点击左上方⚙` -> `新建Class` ->  `类名：Counter` -> ` 点击 正上方 "设置⚙"` ->  `应用key` 获取`app_id`和`app_key`替换_config.yml文件中对应字段

- 主题配置文件~/blog/themes/next/_config.yml配置
```bash
leancloud_visitors:
  enable: true
  app_id: your_app_id
  app_key: your_app_key
```
- 应用安全设置
点击 “安全中心”，在“Web安全域名”中输入自己博客域名，保证数据调用的安全。