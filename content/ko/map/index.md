---
sections:
  - block: markdown
    content:
      title: "School Map"
      subtitle: ''
      text: ''
    design:
      columns: '1'
      background:
        image: 
          filename: map.png
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          height: '1800px'
          text_color_light: true
      css_class: 'position-relative' # position-relative 추가

title: "School Map"
coordinates:
  latitude: '35.8469'
  longitude: '127.1295'
---

<div class="position-relative" style="height: 500px;">
    <iframe 
        width="100%" 
        height="100%" 
        frameborder="0" 
        scrolling="no" 
        src="https://www.openstreetmap.org/export/embed.html?bbox=127.1255%2C35.8464%2C127.1335%2C35.8474&layer=mapnik&marker=35.8469%2C127.1295"
        style="position: absolute; top: 0; left: 0;">
    </iframe>
</div>
