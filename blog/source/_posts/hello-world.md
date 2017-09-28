---
title: Hello World
---

听说程序员都需要写个博客？

作为一个历来标榜自己是“略懂技术的产品”的非专业程序员，一直以来都没兴趣写博客。或者说，也许是因为自己技术渣，写了也只能献丑，所以才不写。

但是万种理由都敌不过生活的无聊，所以还是开始了。

## 使用Hexo

第一篇文章也不知道写点什么，索性就写博客的建立过程。

很早以前就接触过Hexo，那时候刚刚开始用Node.js。选择Github Pages + Hexo方案的原因很简单：可以自由更换主题而且不用自备服务器。

接下来直奔主题。

### 环境依赖

- Git
- Node.js

### 项目搭建

首先创建一个单独的分支（例如：blog）用来维护Hexo项目代码。

``` bash
$ git checkout -b blog
```

新建一个单独的文件夹用来放置Hexo项目文件，然后将当前路劲切换至新创建的项目文件夹。

安装Hexo。

``` bash
$ npm install -g hexo-cli
$ npm install --save hexo

$ hexo init
$ npm install
```

至此，项目环境已准备就绪。

### 项目配置

修改项目文件夹中的`_config.yml`可以实现配置，主要需要设置的是开头Site部分的title、description、author等项。

另外可能需要配置的是结的deploy部分，可以用来配置Git仓库信息，以实现通过`hexo deploy`命令直接部署。

```
deploy:
  type: git
  repo: [repo]
  branch: master
```

### 添加新文章

``` bash
$ hexo new "Post Title"
```

该命令会在`source/_posts`文件夹下创建一个markdown文件作为新文章，内容的修改只需直接编辑文件。

### 生成与预览

``` bash
$ hexo generate
$ hexo server
```

### 使用主题

一般都是将主题项目（通常是Github仓库）clone至themes文件夹下然后修改_config.yml中的配置即可，更多操作和设置可参考主题项目的说明。

## 最后

这个博客就算开始了。


