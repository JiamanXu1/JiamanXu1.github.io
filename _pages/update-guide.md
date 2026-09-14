---
layout: single
title: "如何更新网站内容"
permalink: /update-guide/
author_profile: true
toc: true
toc_label: "本页目录"
---

本网站由 GitHub 仓库 `JiamanXu1/JiamanXu1.github.io` 管理。每次保存并提交修改后，GitHub Pages 会自动重新构建网站，通常几分钟内生效。

## 首次启用自动发布

仓库第一次创建并上传后，进入 **Settings → Pages**，在 **Build and deployment** 下把 **Source** 设为 **GitHub Actions**。之后通常不需要再次设置，推送到 `main` 分支就会自动发布。

## 最简单的方法：直接在 GitHub 网页上修改

1. 登录 GitHub，进入仓库 `JiamanXu1.github.io`。
2. 找到需要修改的文件，点击右上角铅笔图标 **Edit this file**。
3. 修改内容后，点击 **Commit changes**。
4. 等待几分钟，访问 `https://JiamanXu1.github.io` 检查结果。
5. 如果没有更新，打开仓库的 **Actions** 页面，查看最新一次部署是否成功。

## 常用内容分别放在哪里

| 要修改的内容 | 文件或目录 |
| --- | --- |
| 姓名、简介、邮箱、头像、社交账号 | `_config.yml` |
| 首页介绍 | `_pages/about.md` |
| 顶部导航 | `_data/navigation.yml` |
| 个人简历 | `_pages/cv.md` |
| 论文与研究成果 | `_publications/` |
| 学术报告 | `_talks/` |
| 教学经历 | `_teaching/` |
| 代表项目 | `_portfolio/` |
| PDF、压缩包等下载文件 | `files/` |
| 头像及页面图片 | `images/` |

## 修改个人信息与头像

编辑 `_config.yml` 中的 `author` 区域。没有的信息请保持为空，不要删除字段左侧的缩进。

```yaml
author:
  avatar   : "profile.jpg"
  name     : "你的姓名"
  bio      : "一句话研究简介"
  location : "所在城市"
  employer : "学校或机构"
  email    : "name@example.com"
  github   : "JiamanXu1"
```

头像文件上传到 `images/profile.jpg`。文件名必须与 `avatar` 中填写的名称完全一致，包括大小写。

## 新增一篇论文

在 `_publications/` 中创建文件，例如 `2026-09-论文简称.md`。文件开头的三条横线和字段名称必须保留：

```markdown
---
title: "论文标题"
collection: publications
category: conferences
permalink: /publication/2026-paper
excerpt: "一句话摘要"
date: 2026-09-14
venue: "期刊或会议名称"
paperurl: "/files/paper.pdf"
citation: "作者. 论文标题. 期刊或会议, 2026."
---

这里填写摘要、贡献说明或其他正文。
```

`category` 可填写 `books`、`manuscripts` 或 `conferences`。如果提供 PDF，请先上传到 `files/`，再填写 `paperurl`。

## 新增学术报告、课程或项目

最稳妥的方式是参照本页的论文示例，在对应目录中新建 Markdown 文件，再修改文件名及开头的元数据：

- 学术报告：`_talks/`
- 教学经历：`_teaching/`
- 项目：`_portfolio/`

日期推荐统一写为 `YYYY-MM-DD`。`permalink` 必须唯一，并以 `/` 开头。

## 上传和引用文件

把 PDF、幻灯片或压缩包上传到 `files/`。例如上传 `files/cv.pdf` 后，可在任意 Markdown 页面中写：

```markdown
[下载 PDF 简历](/files/cv.pdf)
```

图片放入 `images/`，引用方式如下：

```markdown
![图片说明](/images/example.jpg)
```

建议文件名只使用小写英文字母、数字和短横线，避免空格与中文标点。

## 在本地电脑修改

适合一次更新多个文件时使用：

```bash
git clone https://github.com/JiamanXu1/JiamanXu1.github.io.git
cd JiamanXu1.github.io
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve -l -H localhost
```

浏览器打开 `http://localhost:4000` 预览。确认无误后：

```bash
git add .
git commit -m "更新个人主页内容"
git push
```

## 发布前检查清单

- `_config.yml` 的 `url` 是 `https://JiamanXu1.github.io`
- `_config.yml` 的 `repository` 是 `JiamanXu1/JiamanXu1.github.io`
- YAML 字段使用英文冒号，并保持原有缩进
- 新增文件的 `permalink` 没有重复
- 图片和 PDF 的文件名与链接大小写完全一致
- GitHub **Actions** 中最新部署显示为绿色成功状态

## 修改出错时如何恢复

在 GitHub 中打开出错文件，点击 **History**，找到上一个正常版本并查看修改差异。可以将正确内容复制回来后再次提交。若是部署失败，先在 **Actions** 中打开失败任务，错误信息通常会指出具体文件和行号。
