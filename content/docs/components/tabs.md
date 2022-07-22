---
title: "Tabs"
description: "A single content area with multiple panels, each associated with a header in a list."
lead: "A single content area with multiple panels, each associated with a header in a list."
date: 2021-07-14T13:26:54+01:00
lastmod: 2021-07-14T13:26:54+01:00
draft: false
images: []
menu:
  docs:
    parent: "components"
weight: 610
toc: true
---

Click tabs to swap between content that is broken into logical sections. Tabs come with a horizontal navigation and a simple, clean style.

<div class="preview">
  <link rel="stylesheet" href="/cssui/cssui.min.css">
  <link rel="stylesheet" href="/cssui/cssui.tabs.min.css">

  <div data-tabs role="tablist" aria-label="Sample tabs">
    <input id="tab1" type="radio" name="tab" data-tab role="tab" aria-controls="tab-panel1" checked="checked">
    <input id="tab2" type="radio" name="tab" data-tab role="tab" aria-controls="tab-panel2">
    <input id="tab3" type="radio" name="tab" data-tab role="tab" aria-controls="tab-panel3">
    <nav>
      <label for="tab1" data-tab-label>First Tab</label>
      <label for="tab2" data-tab-label>Second Tab</label>
      <label for="tab3" data-tab-label>Third Tab</label>
    </nav>
    <section id="tab-panel1" data-tab-panel role="tabpanel" aria-labelledby="tab1">
      First Tab Panel
    </section>
    <section id="tab-panel2" data-tab-panel role="tabpanel" aria-labelledby="tab2">
      Second Tab Panel
    </section>
    <section id="tab-panel3" data-tab-panel role="tabpanel" aria-labelledby="tab3">
      Third Tab Panel
    </section>
  </div>
</div>

## Usage

Tabs only require the following structure:
- a `data-tabs` container for both navigation and panels
- use `<input type="radio"` for each navigation link

```html
<div data-tabs role="tablist" aria-label="Sample tabs">
  <input id="tab1" type="radio" name="tab" data-tab role="tab" aria-controls="tab-panel1" checked="checked">
  <input id="tab2" type="radio" name="tab" data-tab role="tab" aria-controls="tab-panel2">
  <input id="tab3" type="radio" name="tab" data-tab role="tab" aria-controls="tab-panel3">
  <nav>
    <label for="tab1" data-tab-label>First Tab</label>
    <label for="tab2" data-tab-label>Second Tab</label>
    <label for="tab3" data-tab-label>Third Tab</label>
  </nav>
  <section id="tab-panel1" data-tab-panel role="tabpanel" aria-labelledby="tab1">
    First Tab Panel
  </section>
  <section id="tab-panel2" data-tab-panel role="tabpanel" aria-labelledby="tab2">
    Second Tab Panel
  </section>
  <section id="tab-panel3" data-tab-panel role="tabpanel" aria-labelledby="tab3">
    Third Tab Panel
  </section>
</div>
```
## Accessibility
You can navigate tabs using keyboard by default. Press TAB it will move the focus on the first tab item. By then, you can move between tabs using the keyboard arrows.

## Variables

List of variables used. Customize the component's design by changing or overriding these values:

```css
  --tab-background: none;
  --tab-label-background: #fff;
  --tab-panel-background: #fff;
  --tab-border-width: 1px;
  --tab-border-hover-width: var(--tab-border-active-width);
  --tab-border-active-width: 2px;
  --tab-panel-border-width: var(--tab-border-width);
  --tab-border-color: #d1d5db;
  --tab-border-hover-color: #9ca3af;
  --tab-border-active-color: #1d4ed8;
  --tab-panel-border-color: none;
  --tab-outline-color: #101010;
  --tab-spacing: 1rem 0.5rem;
  --tab-radius: none;
  --tab-active-shadow: none;
  --tab-transition: opacity 0.3s ease-in-out;
```
