---
title:  Spring boot工程创建
date: 2017-01-11 17:18:07
tags: 
 - spring boot
catagories: 
 - Java
---

### 环境配置

 - Mac OS 10.12.2
 - IntelliJ IDEA 14.0.2(自己网上搜下注册码)
 - [Java SDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

### 创建Sping boot工程

 1. 打开IDEA，File --> New --> Project
 {% asset_img springboot_1.png %}

 2. 点击`Next`,默认工程名为Demo（可以不修改），改名为`testSpring`
{% asset_img springboot_2.png %}

 3. 点击`Next`,选择依赖 
 {% asset_img springboot_3.png %}
 
 4. 点击`Next`，IDEA底部会自动下载依赖库，见底部状态栏下载进度（如没有，请点击图2位置），下载完成显示图1
 {% asset_img springboot_4.png %}
 
 5. 运行，提示如下
{% asset_img springboot_5.png %}

 6. 点开右侧`Maven Projects`边栏
{% asset_img springboot_6.png %}

 7. 报错是由于添加了数据库相关的库而没有配置，所以这里我们先在pom.xml文件中注释掉相关的库，注释掉后如果右侧`Maven Projects` -->`Dependencies`还有数据库相关的包，请点击 图2 刷新，直到显示如 图2所示
{% asset_img springboot_7.png %}

 8. 运行工程，OK
{% asset_img springboot_8.png %}
