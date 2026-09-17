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
        - year: 2024年
          title: >-
            From Dislocation to Creativity: Reflections on Developing a Twine Game Based on Tan’s *The Arrival*
          detail_title: >-
            From Dislocation to Creativity: Reflections on Developing a Twine Game Based on Tan’s *The Strangers*
          summary: >-
            I reflect on the process of deconstructing Shaun Tan’s The Arrival (2006) through game development, the choice of Twine as the medium for creative game-making, and subsequent reflections on how the creation of these materials is deliberately structured for players to develop their game literacy. When designing the game, my aim was to express the theme of dislocation and realise it through integrating game mechanics and achieving recreation in the player’s experience. Drawing inspiration from Tan’s The Arrival, I realised that the concept of dislocation is not merely conveyed through textual narration; rather, it is embodied in abstract visual imagery, dramatic scripting and dynamic scene transitions. Consequently, I structured the game’s deeper significance around elements of partial physical isolation, cultural estrangement and symbolic interpretation. Similar to the protagonist in Tan’s work, players enter an unfamiliar environment where the language, grammar and characters are all foreign to them (Tan, 2006). Their sole means of progression is through repeated encounters and efficient reasoning of fragmented texts, ultimately decoding the true narrative hidden behind various exploratory scenes. In doing so, players engage in affective labour resulting in a profound sense of cultural immersion (Tan, 2006).
          detail: |-
            Creativity is a multifaceted concept defined as the interaction between aptitude, process, and environment through which individuals or groups produce a novel and useful product within a social context (Plucker et al., 2004, p. 90). This definition encompasses four key elements of creativity: 'person', 'process', 'product' and 'press' (environment). I use Rhodes's Four P's model of creativity (Rhodes, 1961) to explain my recreation of the game, albeit with different meanings assigned to each aspect.

            The 'person' aspect focuses on the aptitudes associated with creativity, such as enhancing players' problem-solving and reasoning abilities through gameplay (Runco & Chand, 1995). The 'process' aspect concerns the cognitive and behavioural steps involved in creative thinking and action (Wallach & Kogan, 1965). This is evident in the initial design phase, where I determine the game's narrative flow, conditional 'if' structures and potential outcome pathways.

            The 'product' aspect concerns the usability of the final artefact. In the context of a game, this is achieved through simplified UI design, clearer branching options and richer multimodal representations. Finally, the 'press' aspect considers the influence of society and culture on creativity (Glăveanu, 2015). During production, I incorporate personal experience and cultural background into the creative process (McCallum, 2012).

            Reflecting on my workflow and design decisions, I have organised the Four P's into two categories: establishing game grammar and discourse with a focus on person and press. The second part focuses on process and product, and involves the selection of development tools and the design of game semiosis and ludosis.
          image: media/academic-work-twine.png
          image_alt: Twine game development passage map
          image_position: center
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
      css_class: research-reveal-section
---
