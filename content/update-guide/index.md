---
title: 网站更新指南
date: "2026-09-15"
toc: true
---

这份指南是网站的一部分，请长期保留。本站基于 Hugo Blox 构建，内容主要由 Markdown 和 YAML 文件组成；日常更新不需要修改程序代码。

## 最常用的文件

| 要修改的内容 | 文件或目录 |
|---|---|
| 姓名、身份、单位、个人简介、研究方向 | `content/authors/admin/_index.md` |
| 头像 | `content/authors/admin/avatar.png` |
| 首页结构、各板块标题、视频与遮罩参数 | `content/_index.md` |
| 首页循环背景视频 | `static/media/home-intro.mp4` |
| 视频加载失败时的备用图片 | `assets/media/home-background.jpg` |
| 教育、工作、技能、语言、奖项数据 | `content/authors/admin/_index.md` |
| 研究成果 | `content/publications/` |
| 学术报告 | `content/event/` |
| 教学经历 | `content/teaching/` |
| 项目 | `content/projects/` |
| 网页版简历 | `content/cv/index.md` |
| PDF 简历 | `static/uploads/resume.pdf` |
| 顶部中文导航 | `config/_default/menus.yaml` |
| 网站名称、描述和配色 | `config/_default/hugo.yaml`、`config/_default/params.yaml` |

## 方法一：直接在 GitHub 网页修改

1. 登录 GitHub，进入 `JiamanXu1/JiamanXu1.github.io` 仓库。
2. 打开要修改的文件，点击右上角铅笔图标。
3. 修改后点击 **Commit changes**。
4. 等待仓库的 **Actions** 页面出现绿色对勾。
5. 通常数分钟后刷新 `https://JiamanXu1.github.io/` 即可看到更新。

这是修改少量文字最省事的方法。

## 方法二：在本地修改后推送

首次使用：

```bash
git clone https://github.com/JiamanXu1/JiamanXu1.github.io.git
cd JiamanXu1.github.io
```

以后每次更新：

```bash
git pull
# 修改文件
git add .
git commit -m "Update website content"
git push
```

如已安装 Hugo Extended 与 pnpm，可在推送前本地预览：

```bash
pnpm install
hugo server
```

浏览器访问终端显示的本地地址。确认无误后按 `Ctrl+C` 停止。

## 修改个人资料

打开 `content/authors/admin/_index.md`。文件顶部两条 `---` 之间是结构化资料，第二条 `---` 之后是首页“关于我”正文。

例如将：

```yaml
role: 请填写你的职称、年级或学术身份
organizations:
  - name: 请填写所在学校、院系或研究机构
```

替换为真实信息。添加邮箱时可在 `profiles` 中加入：

```yaml
  - icon: at-symbol
    url: mailto:你的邮箱地址
    label: 邮件
```

请勿把不希望公开的手机号、家庭地址、证件信息写入仓库。

## 更换头像

1. 准备 JPG、JPEG 或 PNG 图片，建议使用正方形或接近正方形的清晰照片。
2. 将新图片命名为 `avatar.png`，替换 `content/authors/admin/avatar.png`。
3. 文件路径和名称不变时，无需修改其他配置。

如果浏览器仍显示旧头像，可强制刷新页面或稍等缓存更新。

## 添加研究成果

在 `content/publications/` 下为每项成果新建一个英文短名称目录，例如：

```text
content/publications/my-first-paper/index.md
```

内容示例：

```yaml
---
title: "论文真实标题"
authors:
  - admin
  - 合作者姓名
date: "2026-01-01"
publishDate: "2026-01-01"
publication: "期刊或会议名称"
publication_types:
  - article-journal
featured: false
doi: ""
url_pdf: ""
---

在这里填写摘要或成果简介。
```

日期必须使用 `YYYY-MM-DD` 格式。`featured: true` 可将成果标为精选。没有 DOI 或 PDF 时保留空字符串即可，不要填写虚构链接。

## 添加学术报告

新建 `content/event/报告短名称/index.md`：

```yaml
---
title: "报告真实标题"
event: "会议或主办方"
location: "城市或线上"
date: "2026-01-01T09:00:00+08:00"
date_end: "2026-01-01T10:00:00+08:00"
all_day: false
---

在这里填写报告简介。
```

## 添加教学经历

新建 `content/teaching/课程短名称/index.md`：

```yaml
---
title: "课程或教学工作名称"
date: "2026-01-01"
summary: "一句话简介"
---

填写课程、职责、授课对象、学期和教学材料等真实信息。
```

## 添加项目

新建 `content/projects/项目短名称/index.md`：

```yaml
---
title: "项目名称"
date: "2026-01-01"
summary: "一句话项目简介"
tags:
  - 研究关键词
external_link: ""
---

填写项目背景、你的职责、采用的方法和成果。
```

如果要显示项目封面，把图片命名为 `featured.jpg` 或 `featured.png`，放在同一个项目目录中。

## 修改简历

网页版简历在 `content/cv/index.md`。直接替换“待补充”文字即可。

如需提供 PDF：

1. 将 PDF 命名为 `resume.pdf`。
2. 上传至 `static/uploads/resume.pdf`。
3. 在简历页或个人资料中加入链接 `/uploads/resume.pdf`。

更新 PDF 时保持文件名不变，原链接会继续有效。

## 更换学术页背景

可以更改，而且目前已经做成易于维护的两层设置。

### 更换首页循环视频

首页目前使用 1920×1080 的 MP4 循环视频。最简单的更换方法是直接替换：

```text
static/media/home-intro.mp4
```

保持文件名不变即可，不需要修改其他文件。建议：

- 使用 H.264 编码的 MP4，分辨率建议为 1920×1080。
- 视频应能无缝循环，建议时长约 5–15 秒。
- 为避免移动端加载过慢，建议文件不超过约 8 MB。
- 视频不会播放声音；首页已设置 `muted`、`loop` 和 `playsinline`。

如果浏览器禁止自动播放或视频尚未加载，网站会使用以下图片作为备用画面：

```text
assets/media/home-background.jpg
```

### 修改遮罩和动画速度

在 `content/_index.md` 的首页首个区块中修改：

```yaml
content:
  video: media/home-intro.mp4
  poster: media/home-background.jpg
design:
  overlay_opacity: 0.80
  overlay_duration: 1200
```

- `overlay_opacity` 是深灰色遮罩的不透明度，范围为 `0` 至 `1`。当前 `0.80` 表示遮住 80% 的背景颜色。
- `overlay_duration` 是遮罩从左向右展开所需的毫秒数，`1200` 即 1.2 秒。
- 遮罩完成后，头像和个人文字才会淡入；随后页面才恢复正常滚动。
- 键盘的向下键、Page Down、空格，以及手机向上滑动，也会触发同样的动画。

完整动画样式与逻辑位于：

```text
layouts/_partials/blox/hero-video.html
```

如果系统开启“减少动态效果”，网站会跳过过渡动画、暂停视频并直接显示内容，以保证无障碍访问。

### 更改普通页面背景

普通页面的浅色与深色背景定义在：

```text
layouts/partials/hooks/head-end/custom.html
```

修改 `--academic-page-bg` 和 `--academic-page-bg-dark` 即可。建议保持文字与背景有足够对比度；修改后同时检查电脑和手机、浅色和深色模式。

## 修改导航栏

导航配置位于 `config/_default/menus.yaml`。`name` 是显示文字，`url` 是链接，`weight` 越小越靠左。例如：

```yaml
  - name: 网站更新指南
    url: update-guide/
    weight: 80
```

## 发布与故障排查

每次推送到 `main` 分支都会触发 `.github/workflows/deploy.yml`。在 GitHub 仓库中打开 **Actions**，绿色对勾表示构建和发布成功。

如果失败：

1. 点击失败的工作流和红色步骤查看错误行。
2. 优先检查 YAML 缩进。YAML 必须使用空格，不能使用 Tab。
3. 确认每个 Markdown 文件开头和结尾的 `---` 成对出现。
4. 检查日期是否加引号并符合格式。
5. 检查文件名和链接中的大小写；GitHub Pages 区分大小写。
6. 修正并再次提交，Actions 会自动重跑。

## 更新前检查清单

- 页面中没有残留“请填写”或不需要的“待补充”文字。
- 姓名、单位、日期、论文作者顺序和链接准确。
- 没有上传隐私信息或不应公开的材料。
- 图片大小合理，建议单张不超过约 2 MB。
- GitHub Actions 构建成功。
- 电脑和手机端均可打开首页、内容页与本指南。
