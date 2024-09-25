---
# Use the Intro widget of the Blog template
widget: about.avatar

# This file represents a page section.
headless: true

# Order that this section will appear in.
weight: 10

author: admin
#design:
#  background:
#    color: '#090a0b'
#    text_color_light: true
#    video:
#      path:  # enter filename of a video in /assets/media
#  css_class: fullscreen

type: landing

sections:
  - block: slider
    content:
      slides:
      - title:  Mobile Network 
        content: 모바일 네트워크는 이동성과 접근성을 제공하며, 5G 기술의 발전으로 빠르고 효율적인 통신을 가능하게 하여 미래의 네트워크 혁신을 이끌고 있습니다.
        align: center
        background:
          image:
            filename: C:\Users\wldne\Desktop\wldnek03.github.io\content\home\computer.jpg
            filters:
              brightness: 0.7
          position: right
          color: '#666'
      - title: LDPC coding
        content: 'Share your knowledge with the group and explore exciting new topics together!'
        align: left
        background:
          image:
            filename: C:\Users\wldne\Desktop\wldnek03.github.io\content\home\LDPC.jpg
            filters:
              brightness: 0.7
          position: center
          color: '#555'
      - title: Network Slicing
        content: 'Just opened last month!'
        align: right
        background:
          image:
            filename: C:\Users\wldne\Desktop\wldnek03.github.io\content\home\slice.jpg
            filters:
              brightness: 0.5
          position: center
          color: '#333'
        link:
          icon: graduation-cap
          icon_pack: fas
          text: Join Us
          url: ../contact/
    design:
      # Slide height is automatic unless you force a specific height (e.g. '400px')
      slide_height: ''
      is_fullscreen: true
      # Automatically transition through slides?
      loop: false
      # Duration of transition between slides (in ms)
      interval: 2000
---

👋 안녕하세요, 저는 **이지우** 입니다. 통신과 네트워크에 관련하여 연구를 하고있습니다. 
{style="font-size: 1.2rem; background: #FFB76B; background: linear-gradient(to right, #FFB76B 0%, #FFA73D 30%, #FF7C00 60%, #FF7F04 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent;"}


저의 [이력서](about/) 와 아래의 포트폴리오를 확인해보세요. ✔️
