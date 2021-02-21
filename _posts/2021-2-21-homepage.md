---
title: '个人网站搭建'
date: 2021-2-21
permalink: /posts/2020/2/homepage/
tags:
  - 中文
  - 个人网站
  - Github Pages
---

对于刚接触科研或者说已经在科研的路上走了一段路程的同学来说，拥有一个漂亮简单的主页是迫切的，当然我也不例外，看见大佬们的主页都觉得好帅啊。鉴于网上的大部分资料对于非计算机或者说没有接触过**github**和**markdown**的同学非常不友好，这里我就做了一个更详细的博客来讲讲我是怎末用3个小时来搭好我的个人主页的。在介绍之前先展示几个用同一个模板写的主页：[大佬1：Tianqi Chen](https://tqchen.com/)， [大佬2：Jian Li](https://lijian.ac.cn/)， [菜鸡本人：李梓强](https://iceli1007.github.io/). 本博客是根据[jian li 同学的博客](https://lijian.ac.cn/posts/2018/11/homepage/)修改而来，去掉了一些关于域名的东西，加入了我在实践过程中的一些详细的介绍。可以供非计算机或者不熟悉相关知识的人使用。

### 1 工具介绍
本博客主要采用两种工具：**git**和**markdown**。
##### 1.1 markdown
markdown是一种便捷化的文档编辑语言，相比latex更加的简便易于上手，主要用在github和简书等平台的文档编写，关于markdown的介绍可以查看[博客](https://www.jianshu.com/p/7771794c88a1). 一般情况我都用markdown来编写文档，给老师写汇报，交作业之类的。当然我带的助教课如果老师没特别要求，我也会要求学生用markdown来编写作业。编写markdown需要编译器，一般情况我会使用vscode来编写markdown，因为vscode有预览功能，非常好用。这里推荐[博客](https://zhuanlan.zhihu.com/p/56943330)。
##### 1.2 git
git是一个非常好用的工具，详细的介绍可以看[博客](https://www.jianshu.com/p/662d9bb9cadc). 我们在这里用的也是比较简单的一些命令，比如git clone ，git add等等。

### 2 模板选择&使用
为什么选择github，主要是简单。为了更简单选择https://academicpages.github.io 给出的学术模板，其具体步骤如下：
1. 注册github账户。
2. 在windows下下载git，详细过程见[博客](https://www.jianshu.com/p/662d9bb9cadc).
3. Fork[该仓库](https://github.com/iceli1007/iceli1007.github.io)。(相当于把我的仓库copy一份到你的主页下)
![](https://github.com/iceli1007/iceli1007.github.io/images/1)
4. 在仓库Setting中修改仓库名称为`[your_name].github.io`，该名称将会成为你个人主页的网址。我的github用户名为iceli1007. 你需要将其修改为你的用户名。
5. 在你的github中下载仓库：需要用到[博客](https://www.jianshu.com/p/662d9bb9cadc)中所述的git clone命令。（譬如要下载我的个人主页仓库，其命令为`git clone https://github.com/iceli1007/iceli1007.github.io`）

接下来就是修改了。
1. 下载vscode。详细过程见[博客](https://zhuanlan.zhihu.com/p/56943330)。
2. 设置侧边内容，侧边内容是在`_config.yml`中配置, 你可以对照我的主页将你自己的信息和照片修改进去。（.yml文件可以用txt格式打开和编辑）
3. 设置顶部内容，顶部菜单在`_data/navigation.yml`中配置，目前我采用的只有 `Publications`，`Teaching`, `CV&Contact` 和`Blogs`四个栏目，你可以根据自己情况删除和增加。 
4. 设置好标题之后我们就需要填内容了。内容文件是markdown文件，其全部存放在`_pages/`文件夹下。这里我用到的文件主要有四个`about.md`, `publications.md`, `teaching.md`, `cv&concat.md`.分别对应着栏目 `aboutme`,`Publications`,`Teaching` 和 `CV&Contact`。我们只需要用vscode打开`.md`文件，并填上自己的内容即可。
5. 最后就是栏目`Blogs`，他没有对应的`.md`文件，这里每一篇blog对应一个`.md`文件都被存放在`_posts/`文件夹下，你可以自己添加博客了。
6. 等所有的修改结束，就可以按照[博客](https://www.jianshu.com/p/662d9bb9cadc)中所述的方法，将仓库从本地更新到云端了：具体命令为 `git add .`, `git commit -m update` 和 `git push origin master`（注意所有的命令都是在你本地仓库文件夹下运行）。

### 3 访问

等仓库更新到云端，说明已经大功告成了，你就可以访问自己的主页了。譬如我的主页为：`https://iceli1007.github.io/`。