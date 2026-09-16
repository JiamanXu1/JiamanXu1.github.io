---
title: ""
date: "2026-09-15"
type: landing
design:
  spacing: 6rem
sections:
  - block: hero-video
    content:
      username: admin
      video: media/home-intro.mp4
      poster: media/home-background.jpg
      scroll_hint: 向下滚动进入主页
      button:
        text: 查看简历
        url: cv/
    design:
      css_class: dark academic-video-section
      overlay_opacity: 0.82
      overlay_duration: 1200
      avatar:
        size: medium
        shape: circle
      spacing:
        padding:
          - 0
          - 0
          - 0
          - 0
  - block: markdown
    content:
      title: 欢迎访问我的学术主页
      text: |-
        本站用于展示个人简介、研究成果、学术报告、教学、项目与简历。所有需要替换的文字均以“请填写”或“待补充”标出，便于后续逐项更新。
  - block: collection
    id: publications
    content:
      title: 研究成果
      text: 论文、预印本和其他研究成果将在这里展示。
      filters:
        folders:
          - publications
    design:
      view: citation
  - block: collection
    id: talks
    content:
      title: 学术报告
      text: 受邀报告、会议报告和学术交流记录将在这里展示。
      filters:
        folders:
          - event
    design:
      view: date-title-summary
  - block: collection
    id: projects
    content:
      title: 项目
      text: 研究项目、开源项目和合作项目将在这里展示。
      filters:
        folders:
          - projects
    design:
      view: article-grid
      columns: 3
---
