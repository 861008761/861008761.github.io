---
layout: post
title: "关于bootstrap的分页的CSS样式控制的代码"
description: ""
category: ""
tags: []
---
关于分页pagination的bootstrap样式的代码，把它放到自己建立的样式表比如style.css中引用即可。

样式控制代码如下
{% highlight xml linenos %}

.pagination li { display: inline; }
.pagination li a { position: relative; float: left; padding: 6px 12px; margin-left: -1px; line-height: 1.428571429; text-decoration: none; background-color: #fff; border: 1px solid #ddd; }
.pagination li:first-child a { margin-left: 0; border-bottom-left-radius: 4px; border-top-left-radius: 4px; }
.pagination li:last-child a { border-top-right-radius: 4px; border-bottom-right-radius: 4px; }
.pagination li a:hover, .pagination li a:focus { background-color: #eee; }
.pagination .active a, .pagination .active a:hover, .pagination .active a:focus { z-index: 2; color: #fff; cursor: default; background-color: #428bca; border-color: #428bca; }
.pagination .disabled a, .pagination .disabled a:hover, .pagination .disabled a:focus { color: #999; cursor: not-allowed; background-color: #fff; border-color: #ddd; }
.pagination-lg li a { padding: 10px 16px; font-size: 18px; }
.pagination-sm li a, .pagination-sm li span { padding: 5px 10px; font-size: 12px; }

{% endhighlight %}

更多关于Jekyll的信息，请访问：[Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.