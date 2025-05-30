---
layout: post
title: "ubuntu18.04安装jekyll"
date: "2022-08-28 20:48:28"
categories: 环境配置
auth: quitino
tags: jekyll 环境配置

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
gem update --system 
#安装jekyll
gem install jekyll
gem install bundler -v '1.17.3'
bundle install
bundle add webrick
jekyll -v #查看版本

#切到博客文件夹下
bundle exec jekyll serve

#浏览器中预览
http://localhost:4000/
```

由于是 `gitclone` 工程文件,因此部分涉及到工程属性的文件可能会有冲突, 执行 `bundle exec jekyll serve` 时报错:

```bash
/home/q/gems/gems/jekyll-4.0.1/lib/jekyll/cache.rb:171:in `load': dump format error for symbol(0x45) (ArgumentError)
```

解决方案: `bundle exec jekyll clean`, 然后在执行  `bundle exec jekyll serve` 



- [参考文档](https://ywnz.com/linuxyffq/4335.html)
- [参考文档](https://matters.news/@kaixdev/37388-ubuntu-18-04-%E5%AE%89%E8%A3%9D-jekyll-bafyreiakfcusg4cg2ljgmylawk4tdcuhpbczs72xugg77p2pvwy3nqlica)
- [参考文档](https://juejin.cn/post/6844903890601639944)
- [参考文档](https://juejin.cn/post/7023735670640214023)



>Q: 为什么预览的时候有这篇文章,上传后不显示呢.  
>A: 每次上传:  
>   bundle exec jekyll clean  
>   bundle exec jekyll serve  
