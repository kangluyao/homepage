---
title: 关于我的个人网站
date: '2021-06-28'
slug: about-my-personal-site
---
>谈我的个人网站的制作过程，主要是想将整个个人网页制作过程记录下来，当一个笔记吧。

我的个人网页是用Hugo 制作的，使用的是 R 包 [blogdown](https://disq.us/url?url=https%3A%2F%2Fgithub.com%2Frstudio%2Fblogdown%3AmAY6yyl-LJyLUHOVCFLTv486H_Q&cuid=2743984)，关于blogdown的使用方法可以参考[谢益辉](https://yihui.org/)大佬写的[blogdown: Creating Websites with R Markdown](https://bookdown.org/yihui/blogdown/)。好了，介绍一下我的主页制作过程吧。

首先，在Rstudio中安装blogdown包，安装好后使用blogdown建立一个project，设置好目录名称和路径，选择Hugo主题。然后运行`blogdown::serve_site()`就可以在Viewer窗口看到网页的雏形。当然，网页的设计布局需要自己通过修改`_layout`和`config.yaml`等文件来实现，详细见谢益辉大佬写的指导书吧。

一种快速且方便的方法是去看看那些设计做的好的网站，然后去他们的 github上将整个网站内容download下来 ，然后仔细研究他们的`_layout`，`CSS`和`_config.yml`文件。很多人会将自己的个人主页托管到GitHub上，可以直接在他们的GitHub上下载下来。我比较推荐这个方法，我自己对网页设计不是很在行，所以通过借鉴修改别人的优秀设计，然后搭建自己的网站。这种方法对于没有网页设计基础的人比较友好。我本人的个人主页是端了我的师兄[李代江](https://daijiang.name/)的个人主页，然后修改了域名，`_layout`，`_config.yml`以及其他一些文件之后做成的。也不知道我师兄会不会说我侵犯了他的知识产权，哈哈，不管了，我是他的小迷弟呢！

接下来是发布网站，即将制作好的个人主页上载到服务器上，获得相应的域名，这样别人就能通过访问域名查看你的个人主页了，我采用的是Netlify(https://www.netlify.com)。Netlify提供了一个免费的计划，实际上有很多有用的功能。如果之前没有发布网站的经验，只需要用GitHub账号或者其他账号登录，把blogdown为网站生成的`public/folder`文件拖拽到Netlify页面，几秒钟后网站就可以上线了，随机获得子域名，可以修改这个域名。再将这个域名写入到`_config.yml`文件中，这样别人就可以通过该域名访问网站了。

使用Netlify发布网站存在一个非常不方便的问题，当我写了一篇日志需要上载的时候，我需要重新发布我的网站，这使得整个过程显得非常麻烦，对于网站的管理非常不便捷。我的解决办法是将自己的网站文件上载到我的GitHub上的`homepage`，然后在Netlify和`homepage`之间建立联系，使Netlify获得读取`homepage`的权限。然后每次只需要写好日志，使用github desktop推送到`homepage`，个人主页中就会同步日志了，so easy!

到这里网页基本上就差不多了，just enjoy it!

