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
  - block: academic-gallery
    content:
      title: 欢迎访问我的学术主页
      items:
        - year: xxxx年
          title: 名称
          summary: 学术作品摘要呈现
          detail: |-
            学术作品详细内容呈现
          image: ""
        - year: xxxx年
          title: 名称
          summary: 学术作品摘要呈现
          detail: |-
            学术作品详细内容呈现
          image: ""
        - year: xxxx年
          title: 名称
          summary: 学术作品摘要呈现
          detail: |-
            学术作品详细内容呈现
          image: ""
        - year: xxxx年
          title: 名称
          summary: 学术作品摘要呈现
          detail: |-
            学术作品详细内容呈现
          image: ""
    design:
      css_class: academic-gallery-section
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
