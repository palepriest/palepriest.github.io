---
file: guide-for-pkm.md
title: "Sharing workflow of digital gardening"
date: 2023-04-04
lastmod: 2023-04-11
draft: false
garden_tags: [""]
summary: "Simple workflow and guide on digital gardening."
status: "seeding"
---

> 目标读者：了解过 “个人知识管理”，“打造第二大脑” 或者 “数字花园” 等概念，以及对记笔记和写作感兴趣的人。

听过很多道理，却依然过不好这一生，前辈们分享的工具也很多，使用之后总觉得繁琐，所以想要分享自用的工作流，同时给读者朋友们提供参考，寻找满足需求的平替，构建适用于自己的信息管理模式。

**分析**

- 用户特征：职业是软件开发，日常接触的信息多与 [[编程，设计]] 相关
- 工具需求：
    - 全平台，优先本地存储，迁移成本低，比如 obsidian 的纯文本
    - 核心功能简单易用，比如 flomo 的记录， Hypothesis 的标注
    - 扩展性强，社区活跃，比如 obsidian 的插件，界面美观（非必要）
- 实际场景：线下闲聊，地铁听书，网上冲浪，掌灯夜读

根据日常活动列出场景，发现信息管理和知识管理并不冲突，区别在于处理 meta-data 的方式不同。如果在他们之间建立弱关联，就是信息管理，如果建立强关联，类似大浪淘沙形成金子般稳定的产物，大概就是知识管理。

**工作流**

参考 Input - Process - Output 模型，将信息管理划分成以下三个阶段：

<img src=./workflow-of-digital-gardening.svg width=100% />

- 采集
    - [Flomo](https://flomoapp.com/) 记录想法（Thoughts），通过工具发送到知识库的 [[备忘录]]
    - [ReadKit](https://readkit.app/) 订阅信源（RSS Feeds），优质信源可以参考 [[信源列表]]
    - [Raindrop.io](http://Raindrop.io) 书签管理（Bookmarks），比如 [[云上书签]]
    - [Notion](https://www.notion.so/product) 书籍管理（PDFs，EPUBs），比如 [[电子书库]]
    - [Cubox](https://cubox.pro/) 稍后读（Read-it-Later），可以剪藏网页，也可以订阅期刊
    - [Hypothesis](https://web.hypothes.is/) 网页标注（Web-Highlighting），通过工具同步到知识库
    - [Readwise/Reader](https://readwise.io/read) 全能软件（All-in-One），订阅价格较高，非必要
- 处理
    - [Obsidian](https://obsidian.md/) 知识库（Knowledge Base），整合观点，输出内容
    - Plugins：Excalidraw，Hypothesis，Readwise 以及各类同步插件
    - Tools：使用专业工具实现想法，比如 Procreate 绘制 [[生活指南]]
- 分享
    - Hugo + Github Pages 托管 [个人博客](https://palepriest.github.io/)

**结尾**

随着 LLM 模型和衍生 AI 的加速发展，“知识管理” 在将来也许会被重塑，但是使用工具的 <u>过程和经验</u> 总是值得借鉴的，朋友们下期再见！