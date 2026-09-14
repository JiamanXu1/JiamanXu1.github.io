---
layout: archive
title: "个人简历"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

简历内容正在整理中。你可以直接编辑本文件（`_pages/cv.md`），也可以将 PDF 简历上传到 `files/` 目录后，在此添加下载链接。

教育经历
======

待补充。

工作与研究经历
======

待补充。

研究成果
======

<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

学术报告
======

<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>

教学经历
======

<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
