---
# A section created with the Portfolio widget.
# This section displays content from content/project/.
# See https://docs.hugoblox.com/widget/portfolio/

widget: portfolio

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

title: ''
subtitle: ''

sections:
  - block: slider
    content:
      slides:
      - title: 👋 Welcome to the group
        content: Take a look at what we're working on...
        align: center
        background:
          image:
            filename: computer.jpg
            filters:
              brightness: 0.7
          position: right
          color: '#666'
      - title: Lunch & Learn ☕️
        content: 'Share your knowledge with the group and explore exciting new topics together!'
        align: left
        background:
          image:
            filename: LDPC.jpg
            filters:
              brightness: 0.7
          position: center
          color: '#555'
      - title: World-Class Semiconductor Lab
        content: 'Just opened last month!'
        align: right
        background:
          image:
            filename: slice.jpg
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
      is_fullscreen: false
      # Automatically transition through slides?
      loop: false
      # Duration of transition between slides (in ms)
      interval: 2000

content:
  # Page type to display. E.g. project.
  page_type: project

  # Default filter index (e.g. 0 corresponds to the first filter_button instance below).
  filter_default: 0

  # Filter toolbar (optional).
  # Add or remove as many filters (filter_button instances) as you like.
  # To show all items, set tag to "*".
  # To filter by a specific tag, set tag to an existing tag name.
  # To remove the toolbar, delete the entire filter_button block.      

  filter_button:
    - name: All
      tag: '*'
    - name: LDPC coding
      tag: ML
    - name: Mobile Network
      tag: CV
    - name: Network Slicing
      tag: NLP
      
design:
  columns: '1'
  view: masonry
  flip_alt_rows: true
  background: {}
  spacing: {padding: [0, 0, 0, 0]}
---
