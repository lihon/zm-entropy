# ZM熵增

赛博朋克风格轻量静态博客，纯 HTML + CSS + 少量 JS 渲染 Markdown。

## 本地预览

需要启动本地服务器（因为需要 fetch .md 文件）：

```bash
python -m http.server 8000
# 访问 http://localhost:8000
```

## 写新文章

1. 在 `posts/` 目录新建 `.md` 文件，格式如下：

```markdown
---
title: 文章标题
date: 2026-07-15
tags: 标签1, 标签2
excerpt: 文章摘要（显示在首页）
---

正文内容（Markdown 格式）...
```

2. 在 `index.html` 的文章列表中添加对应条目，链接到 `post.html?p=文件名（不带后缀）`

## 部署到 GitHub Pages

```bash
git init
git add .
git commit -m "init: ZM熵增 blog"
git branch -M main
git remote add origin git@github.com:你的用户名/仓库名.git
git push -u origin main
```

在仓库 **Settings → Pages** 选择 `main` 分支，保存即可。

## 技术栈

- HTML + CSS（赛博朋克主题，暗色模式）
- [marked.js](https://github.com/markedjs/marked)（Markdown 渲染，CDN 引入）
- Markdown frontmatter（文章元数据）
- Emoji 短码支持（`:smile:` → 😄）
- 零构建工具、零框架
