---
layout: post
title: "Have a blog site for yourself"
author: Cetus Li
date: 2021-01-20
---
#### <b>拥有自己博客网站的最简方案：</b>
1. 注册 Github 账号，并在浏览器上登录 Github [官网][github]
2. 选择网站[模板][gh-themes]，进入模板的仓库页面后，点击右上角 `Fork`
3. 在自己的 Github 中，找到并打开上一步所 fork 的仓库，进入 `Settings` 选项
4. 按 `<yourUserName>.github.io` 格式对仓库重命名，刷新网页
5. 几分钟后，访问网址 https://yourUserName.github.io/ ，若有页面恭喜你拥有了自己的博客网站
6. 修改 `_config.yml` 和 `_posts/xxxx-xx-xx-yyyyyy.md`，将占位内容替换成自己的信息和博客内容
7. 开始你的写博之旅吧

#### <b>技术原理：</b>
在 Github 建立仓库 `<yourUserName>.github.io` ，就可以拥有自己的博客网站是 Github 一个名为 `Github Pages` 的子项目的功能。

GitHub Pages 是一个静态网站托管服务，它直接从GitHub上的仓库中获取HTML、CSS和JavaScript文件，通过背后集成的 Jekyll 引擎构建最终的网页，并在用户专有子域名`https://yourUserName.github.io/`发布网站 [官方文档][github-pages]

你的 `<yourUserName>.github.io` 仓库中的文件构建了你的网站。文件结构由 Jekyll 生成，了解各个文件的功能请见 [目录结构][file-structure]

-------------
#### <b>题外话：</b>
Github 的核心是一个 git 服务器，除了通过网页访问，还可以使用 `git客户端` 访问。

##### <b>使用git客户端管理仓库：</b>
 - Linux 用户可在 bash 里使用 `git` 命令连接 Github 服务器管理仓库，编辑器自选
 - Windows 用户推荐使用 Sublime Merge ，不推荐使用 Github Desktop，编辑器自选

##### <b>管理仓库的最简方法：</b>
 - 打开浏览器 -> 登录 Github -> 对仓库增删改查、对文件编辑预览
 - <b>All functions are fully covered on website</b>





















[github]: https://github.com/
[gh-themes]: https://pages.github.com/themes/
[file-structure]: https://www.jekyll.com.cn/docs/structure/
[github-pages]: https://docs.github.com/en/github/working-with-github-pages/about-github-pages
