---
# A section created with the Portfolio widget.
# This section displays content from content/project/.
# See https://docs.hugoblox.com/widget/portfolio/

widget: portfolio

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

title: 'Projects'
subtitle: 'Explore our recent projects'

content:
  # Page type to display. E.g. project.
  page_type: project

  # Default filter index (e.g. 0 corresponds to the first filter_button instance below).
  filter_default: 0

  # Filter toolbar (optional).
  filter_button:
    - name: All
      tag: '*'
    - name: LDPC coding
      tag: AI
    - name: Mobile Network
      tag: CV
    - name: Network Slicing
      tag: NLP

design:
  columns: '1'
  view: masonry
  flip_alt_rows: true
  background: {}
  spacing: 
    padding: [0, 0, 0, 0]

block:
  - block: collection
    content:
      title: 'Projects'
      subtitle: ''
      text: ''
      count: 5
      filters:
        author: ""
        category: ""
        exclude_featured: false
        publication_type: ""
        tag: ""
      offset: 0
      order: desc
      page_type: pro
    design:
      view: card
      columns: "1"
---
