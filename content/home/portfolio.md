---
# A section created with the Portfolio widget.
# This section displays content from `content/project/`.
# See https://docs.hugoblox.com/widget/portfolio/
.search-container :
    display: flex;
    align-items: center;
    border: 1px solid #ccc;
    padding: 5px;
    border-radius: 25px;
    width: 300px;
    margin: 0 auto;

.search-container i :
    font-size: 16px;
    color: #888;
    margin-right: 10px;

.search-input:
    border: none;
    outline: none;
    flex-grow: 1;
    padding: 5px;

.search-btn :
    background-color: #007BFF;
    color: white;
    border: none;
    border-radius: 25px;
    padding: 5px 10px;
    cursor: pointer;

.search-btn:hover:
    background-color: #0056b3;

widget: portfolio

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 20

title: ''
subtitle: ''

content:
  # Page type to display. E.g. project.
  page_type: project

  # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  filter_default: 0

  # Filter toolbar (optional).
  # Add or remove as many filters (`filter_button` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove the toolbar, delete the entire `filter_button` block.
  filter_button:
    - name: All
      tag: '*'
    - name: LDPC coding
      tag: ML
    - name: Computer Network
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
