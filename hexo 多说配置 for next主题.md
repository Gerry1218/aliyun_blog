---
title: hexo 多说配置 for next主题
date: 2016-11-09 16:30:00
tags: 
 - next主题
 - hexo
 - 多说
catagories: hexo
---


## next主题配置评论

- 配置`/blog/themes/next/_config.yml`文件
```bash
duoshuo_shortname: code1928
```

- 登录多说http://duoshuo.com/, 创建站点 

- 站点名 `code1928`

- 通用代码如下：
```bash
<!-- 多说评论框 start -->
	<div class="ds-thread" data-thread-key="请将此处替换成文章在你的站点中的ID" data-title="请替换成文章的标题" data-url="请替换成文章的网址"></div>
<!-- 多说评论框 end -->
<!-- 多说公共JS代码 start (一个网页只需插入一次) -->
<script type="text/javascript">
var duoshuoQuery = {short_name:"code1928"};
	(function() {
		var ds = document.createElement('script');
		ds.type = 'text/javascript';ds.async = true;
		ds.src = (document.location.protocol == 'https:' ? 'https:' : 'http:') + '//static.duoshuo.com/embed.js';
		ds.charset = 'UTF-8';
		(document.getElementsByTagName('head')[0] 
		 || document.getElementsByTagName('body')[0]).appendChild(ds);
	})();
	</script>
<!-- 多说公共JS代码 end -->
```

替换`data-thread-key`、`data-title`、`data-url`字段值
```bash
<div class="ds-thread" data-thread-key="<%- page.path %>" data-title="<%- page.title %>" data-url="<%- page.permalink %>"></div>
```
拷贝修改后的内容。

- 替换`comments.swig`文件内容
打开`~/blog/themes/next/layout/_partials/comments.swig`文件，替换其内容。

- 部署 over 


