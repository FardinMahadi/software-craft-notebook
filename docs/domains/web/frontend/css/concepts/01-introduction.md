---
title: CSS Introduction
status: draft
last_reviewed: 09-11-2025
---

# CSS Introduction

CSS (Cascading Style Sheets) describes how HTML elements are presented on screen, paper, or other media.

## Why CSS Matters

- Separates content (HTML) from presentation, making layouts easier to evolve.
- Enables responsive design, theming, and accessibility improvements without changing markup.
- Reduces duplication by centralizing shared styles.

## Real-World Scenario

- A marketing team wants to refresh the look of a product landing page without touching core HTML rendered by the CMS. By adjusting a shared stylesheet, the team can roll out new branding colors and typography across dozens of pages overnight, leaving the content team focused on messaging instead of markup updates.

## First Style Sheet

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Welcome</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Hello CSS</h1>
    <p>Styling and structure now live in separate files.</p>
  </body>
</html>
```

```css
body {
  font-family: system-ui, sans-serif;
  color: #0f172a;
}
```

## Follow-up

- Create a simple HTML page and attach an external CSS file.
- Experiment with changing font, color, and background to see immediate impact.
