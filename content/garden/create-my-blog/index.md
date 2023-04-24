---
title: "Creating my blog"
date: 2023-03-26T14:17:57+08:00
lastmod: 2023-03-26T15:17:57+08:00
draft: false
garden_tags: [" "]
summary: "Simple guide about creating blog based on hugo and github-pages."
status: "seeding"
---

互联网的起源可以追溯到二十世纪六十年代，原型是名为 ARPANET 的计算机网络，旨在为各大学和研究机构之间提供信息共享的平台。发展到现在，他已经成为人们日常工作和生活的重要组成部分，创建个人博客算是探索互联网的方式之一，下面简单介绍使用 hugo + github-pages 创建博客的过程。

**准备工作**

-   安装版本控制软件 [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) 和 [go](https://go.dev/doc/install) 语言环境
    ```bash
    # Open the Git Bash and run: 
    $ git version
      ...
    $ go version
      ...
    ```
    
-   安装 windows 包管理器 [scoop](https://scoop.sh/)
    ```bash
    # Open the PowerShell terminal (version 5.1 or later) and run:
    $ scoop --version
      ...
    
    # Optional: Need to run a remote script the first time
    $ Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    $ irm get.scoop.sh |iex
    ```
    
-   安装静态站点框架 [hugo](https://gohugo.io/installation/windows/) (extended edition)
    ```bash
    # Open a Git Bash and run: 
    $ scoop install hugo-extended
      ...
    $ hugo version
      ...
    ```

**基本操作**

-   创建站点，在本地生成对应的目录
    ```bash
    # create new site
    $ hugo new site hugo-blog
    ```
    
-   下载喜欢的主题，使用 git-submodule 更新
    ```bash
    # download theme
    $ git submodule https://github.com/paulmartins/hugo-digital-garden-theme.git themes/digital-garden
    # update theme
    $ git submodule update --recursive
    
    # copy default config to config.toml
    ```
    
-   创建文章，使用 markdown 编辑内容
    ```bash
    # create new blog
    $ hugo new garden/first.md
    ```
    
-   本地实时预览修改的效果，校对后生成发布文件
    ```bash
    # local preview
    $ hugo server -D
      ...
      Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)

    # publish the static files at ./public
    $ hugo  
    ```
    
-   提交文件到 main branch，首次需要关联远程仓库
    ```bash
    # link remote repository for first time
    $ git init
    $ git branch -M main
    $ git remote add origin https://github.com/palepriest/palepriest.github.io.git

    # upload file as backups
    $ git add .
    $ git commit -m "<your_comment>"
    $ git push -u origin main
    ```
    
-   通过 [github-actions](https://gohugo.io/hosting-and-deployment/hosting-on-github/) 部署到 gh-page branch
    ```yaml
    # change permission: [Setting] > [Workflow permission] > [Allow R/W] 
    github_token: ${{ secrets.GITHUB_TOKEN }}
    ```

**结尾**

台子搭好了，自然就有个问题 “<u>博客写什么</u>”，篇幅有限，我们下期再见！