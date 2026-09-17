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
        url: uploads/xu-jiaman-cv.pdf
        new_tab: true
    design:
      css_class: dark academic-video-section
      overlay_opacity: 0.80
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
        本站用于展示个人简介、学术经历与研究成果。所有需要替换的文字均以“请填写”或“待补充”标出，便于后续逐项更新。
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
---
