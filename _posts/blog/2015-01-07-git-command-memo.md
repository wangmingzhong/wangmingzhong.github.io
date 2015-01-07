---
layout: post
title: "git 常用命令总结与备忘"
modified:
categories: blog
excerpt:
tags: [git]
image:
comments: true
share: true
date: 2015-01-07T14:00:00 +08:00
---


## git 常用命令总结与备忘

{% highlight java %}
    public class HelloWorld {
        public static void main(String[] args) {
            System.out.println("Hello, World");
            System.out.println("blog.ipaler.com");
        }
    }
{% endhighlight %}

导入远程仓库
$ git clone https://github.com/ipaler/test1.git

提交本地代码（master）
$ git status                               : 新增，编辑的文件列表显示
$ git add 文件名                           : 加入commit队列
$ git commit -m '说明文字'                 : 提交文件

切一个新的branch
     $ git checkout -b branch名         : 切一个新的branch，并且向新的brach移动

同时显示更新的文件列表。
     $ git branch                               : branch状态确认。

修改，增加文件

     $ git status                               : 新增，编辑的文件列表显示
     $ git diff 文件名                        : 更新确认   
     $ git add 文件名                       : 加入commit队列
          $ git add -u *                           : 更新的文件批量更新
          $ git reset HEAD 文件名            : 从commit队列删除
     $ git commit -m '说明文字'        : 提交文件
修改的代码还原

    $ git reset --hard HEAD    : 本地的所有代码回到修改前的状态
    $ git checkout 文件名       : 指定文件回到上次commit的状态

代码提交
    $ git push orgin branch名              ：将代码提交到服务器，必须先commit


获取最新代码（在master下更新代码）

     $ cd /home/dev/kg_source/slamdunk/trunk
     $ git ch master
     $ git pull --rebase                           :将最新代码从服务器获取到本地master
     $ git ch branch名
     $ git rebase master                        ：将最新代码合并到当前branch
     $ git push --force origin branch名   : 将本地branch提交到测试用服务器
查看远程有多少分支    $ git remote show origin



…or create a new repository on the command line

touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/wangmingzhong/qrcode.git
git push -u origin master
…or push an existing repository from the command line


git remote add origin https://github.com/wangmingzhong/qrcode.git
git push -u origin master
…or import code from another repository

You can initialize this repository with code from a Subversion, Mercurial, or TFS project.


