---
title: Spring boot之Hello world
date: 2017-01-12 10:54:46
tags: 
 - spring boot
catagories: 
 - Java
---

1. 在`/src/main/java/com.test/`下新建`web`包

2. 在`web`包新建`Java Class`,名为`HomeController`

3. 添加`test`方法,运行工程
{% asset_img springboot2_1.png %}

4. 打开浏览器，地址栏：`http://localhost:8080/test`
{% asset_img springboot2_2.png %}

> **说明**：
> @RestController --- 组合@ResponseBody和@Controller注解；
> @RequestMapping --- 处理请求地址映射的注解，可用于类或方法上。value：     指定请求的实际地址；method：  指定请求的类型， GET、POST、PUT、DELETE等；
> @Controller --- 声明控制器，辅助实现组件扫描，组件扫描器会自动找到HomeController并将其声明为Spring应用上下文中的一个bean(`Spring 实战第4版P143-144`)。
> @ResponseBody --- 将Controller的方法返回的对象，通过适当的HttpMessageConverter转换为指定格式后，写入到Response对象的body数据区。根据Request对象header部分的Accept属性（逗号分隔），逐一按accept中的类型，去遍历找到能处理的HttpMessageConverter;
> @RequestBody --- 读取Request请求的body部分数据，使用系统默认配置的HttpMessageConverter进行解析，然后把相应的数据绑定到要返回的对象上，再把HttpMessageConverter返回的对象数据绑定到 Controller中方法的参数上。
