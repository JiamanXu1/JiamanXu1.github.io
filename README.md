# JiamanXu1.github.io

Jiaman Xu 的个人学术主页，基于 Hugo Blox 构建并通过 GitHub Actions 自动部署到 GitHub Pages。

## 内容原则

- 站点不包含参考模板作者的个人履历或学术成果。
- 未提供的个人内容使用“请填写”或“待补充”标记。
- 网站内置完整中文维护说明：发布后访问 `/update-guide/`。

## 本地预览

需要 Hugo Extended 0.157.0、Node.js 20 和 pnpm：

```bash
pnpm install
hugo server
```

## 部署

推送到 `main` 分支后，`.github/workflows/deploy.yml` 会自动构建并部署。线上地址：<https://JiamanXu1.github.io/>

## 模板说明

本网站的视觉结构参考了 [BlackiePiggy.github.io](https://github.com/BlackiePiggy/BlackiePiggy.github.io)，并重新编写全部个人内容与配置。参考仓库和 Hugo Blox 相关代码按其许可证使用，详见 `LICENSE.md`。

