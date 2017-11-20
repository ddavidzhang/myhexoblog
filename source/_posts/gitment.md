---
title: gitment
date: 2017-11-21 00:52:47
categories:
- blog
tags:
- blog
---
## gitment

**gitment** 是[Sun][https://imsun.net/posts/gitment-introduction/]借助github的issues 做的评论组件，在duoshuo服务停用和disqus需要翻墙的境况下，gitment不失为一种暂时的评论技术方案。关于hexo的next主题如何引进gitment，[这里][http://colabug.com/273427.html] 有比较详细的介绍，但有些复杂，其实现在gitment已被next加入配置直接支持，引入其实非常简单。

- 注册github application

  > 点击<https://github.com/settings/applications/new>注册，注意`Authorization callback URL`填自己的网站url 如 `http://mocksaber.com`.记下**Client ID**和**Client Secret**.

- 修改 `themes/next/_config.yml`  

  ```
  393 # Gitment
  394 # Introduction: https://imsun.net/posts/gitment-introduction/
  395 # You can get your Github ID from https://api.github.com/users/<Github username>
  396 gitment:
  397   enable: true
  398   mint: true # RECOMMEND, A mint on Gitment, to support count, language and proxy_gateway
  399   count: true # Show comments count in post meta area
  400   lazy: true # Comments lazy loading with a button
  401   cleanly: false # Hide 'Powered by ...' on footer, and more
  402   language: # Force language, or auto switch by theme
  403   github_user: yourgithubname # MUST HAVE, Your Github name
  404   github_repo: BlogComments # MUST HAVE, The repo you use to store Gitment comments
  405   client_id: clientId # MUST HAVE, Github client id for the Gitment
  406   client_secret: clientSecret 


  ```

- 正常来说就可以了，重新部署后对有个显示评论的按钮，现在没篇文章都需要做初始化，后面看gitment的作者有没有后续的简单解决方案。