---
layout: post
title: "Blog by Jekyll"
author: Cetus Li
date: 2021-01-20
---
### <b>拥有自己博客网站的最简方案：</b>
1. 注册 Github 账号，并在浏览器上登录 Github
2. 选择网站 [模板][gh-themes]，点击进入该模板的仓库页面后，点击右上角`Fork`，打开自己 Github 的仓库页面，观察是否存在上一步 fork 的仓库，若没有就刷新页面
3. 打开上一步所 fork 的仓库，进入`Settings`选项，按 `<yourUserName>.github.io` 的格式对仓库重命名，刷新网页
4. 几分钟后，访问网址 https://yourUserName.github.io/ ，如果打开后是一个美观的网页，那就恭喜你拥有了自己的博客网站
5. 你的`<yourUserName>.github.io`仓库中的文件构建了你的博客网站。修改 `config.yml` 和 `_posts/xxxx-xx-xx-yyyyyy.md` 中的内容，将占位内容替换成自己的信息和博客内容,即可开始你的写博之旅

>Github 的核心是一个`git`服务器，除了通过网页访问，还可以使用git客户端访问。

### <b>使用git客户端管理仓库：</b>
 - Linux 用户可在`bash`里使用`git`命令连接 Github 服务器进而管理仓库，使用 Vim 等文本编辑器写博客，也可选择带预览功能的编辑器
 - Windows 用户推荐使用 `Sublime Merge` 连接 Github 服务器来管理仓库，不推荐使用 `Github Desktop`，使用 VS Code 或 Sublime Text3 等编辑器写博客，也可选择带预览功能的编辑器
 - 最方便的当然还是网页访问：打开浏览器 -> 登录`Github` -> 对仓库增删改查、对文件编辑预览。<b>All functions are fully covered on website</b>






















[gh-themes]: https://pages.github.com/themes/
