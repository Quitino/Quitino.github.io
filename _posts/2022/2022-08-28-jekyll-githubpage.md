---
layout: post
title: "鸡生蛋蛋生鸡"
date: "2022-08-28 20:48"
categories: 随笔
auth: quitino
tags: jekyll

---
* content
{:toc}
昨晚折腾几小时，想复杂了。还是该早点睡觉的，脑袋晕了就该睡了，第二天再弄。




## jekyll安装



```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install make build-essential
sudo apt-get install ruby ruby-dev
#添加环境变量
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
#安装jekyll
gem install jekyll bundler
bundle install
jekyll -v #查看版本

#切到博客文件夹下
bundle exec jekyll serve

#浏览器中预览
http://localhost:4000/
```



- [参考文档](https://ywnz.com/linuxyffq/4335.html)
- [参考文档](https://matters.news/@kaixdev/37388-ubuntu-18-04-%E5%AE%89%E8%A3%9D-jekyll-bafyreiakfcusg4cg2ljgmylawk4tdcuhpbczs72xugg77p2pvwy3nqlica)






```

```
