---
layout: page
title: 关于
permalink: /about/
icon: heart
type: page
---

* content
{:toc}


## 个人简介

我是冯波，网名路古/Quitino.

这是我的weblog。内容上，目前刚开始建站,还未完善:




- 书影音
- 跑步
- 收藏
- 链接







## 建站缘由


自 2022 年 08 月 27 日起，本站已运行 <span id="days"></span> 天，截至 {{ site.time | date: "%Y 年 %m 月 %d 日" }}，写了博文 {{ site.posts.size }} 篇，{% assign count = 0 %}{% for post in site.posts %}{% assign single_count = post.content | strip_html | strip_newlines | remove: ' ' | size %}{% assign count = count | plus: single_count %}{% endfor %}{% if count > 10000 %}{{ count | divided_by: 10000 }} 万 {{ count | modulo: 10000 }}{% else %}{{ count }}{% endif %} 字。

## 感谢

从简书到Jekyll文章的转换，我使用了Lework的一个Python script（[文章链接](https://lework.github.io/2019/06/15/jianshu-to-jekyll/)）。


## 联系我


## 捐赠

若您觉得本博客所创造的内容对您有所帮助，可考虑略表心意，支持一下。

{% include reward.html %}

## 本页历史


{% include comments.html %}

<script>
var days = 0, daysMax = Math.floor((Date.now() / 1000 - {{ "2022-08-27" | date: "%s" }}) / (60 * 60 * 24));
(function daysCount(){
    if(days > daysMax){
        document.getElementById('days').innerHTML = daysMax;
        return;
    } else {
        document.getElementById('days').innerHTML = days;
        days += 10;
        setTimeout(daysCount, 1);
    }
})();
</script>
