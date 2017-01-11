---
title:  iOS逆向问题集锦
date: 2016-11-21 11:20:00
tags: 
 - iOS逆向
catagories: 
 - 逆向工程
---

### 问题
Q: 安装IOSOpenDev失败  
A: 打开XCode，看下是否已存在 iOSOpenDev分类，已存在的话 说明安装成功了。


Q：Entitlements.plist 文件格式  
A：格式如下:
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple Computer//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<!--
   Entitlements.plist
   test

   Created by user on 16/11/14.
   Copyright (c) 2016年 iDream. All rights reserved.
-->
<plist version="1.0">
    <dict>
    
    <key>keychain-access-groups</key>
    <array>
      <string>Y7MZCY7B7M.*</string>   
    </array>
    <key>get-task-allow</key>
    <true/>
    <key>application-identifier</key>
    <string>Y7MZCY7B7M.*</string>
    <key>com.apple.developer.team-identifier</key>
    <string>Y7MZCY7B7M</string>
    </dict>
</plist>
```


Q：能否直接对导出的.app 直接签名安装   
A：经测试，导出的.app文件不解密，直接签名是无法运行的。


Q：是否需要生成推送证书  
A：不需要

Q: 如何查看页面属于哪个类  
A: reveal工具

Q: 插入的动态库是否可以联调  
A: 可以，打开xcode, `Debug -> Attach to Progress by PID or Name...[Attach to Progress]`, 输入`WeChat`





注： `yololib xxx x.dylib` 执行多次会插入`x.dylib`多次。
