# Jiaman Xu 的个人学术主页

本仓库用于发布 `https://JiamanXu1.github.io`，基于 [Academic Pages](https://github.com/academicpages/academicpages.github.io) 构建。

## 更新内容

- 全站个人信息：编辑 `_config.yml`
- 首页：编辑 `_pages/about.md`
- 简历：编辑 `_pages/cv.md`
- 论文、报告、教学与项目：分别编辑 `_publications/`、`_talks/`、`_teaching/`、`_portfolio/`
- 图片：上传到 `images/`
- PDF 等附件：上传到 `files/`

完整的中文操作说明见网站页面 `_pages/update-guide.md`，发布后访问 `https://JiamanXu1.github.io/update-guide/`。

## 自动发布

推送到 `main` 分支后，`.github/workflows/deploy-pages.yml` 会构建并部署网站。首次使用时，请在仓库 **Settings → Pages → Build and deployment → Source** 中选择 **GitHub Actions**。

## 本地预览

```bash
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve -l -H localhost
```

浏览器打开 `http://localhost:4000`。
