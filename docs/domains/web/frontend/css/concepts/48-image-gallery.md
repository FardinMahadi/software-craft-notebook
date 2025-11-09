---
title: CSS Image Galleries
status: draft
last_reviewed: 09-11-2025
---

# CSS Image Galleries

## Why It Matters

- Galleries showcase multiple images; CSS handles layout and interaction without heavy scripts.

## Core Ideas

- Use grid (`auto-fit/auto-fill`) for responsive columns.
- Combine `aspect-ratio` and `object-fit` to keep images tidy.
- Add hover overlays or transforms for interactivity while keeping captions accessible.

## Real-World Scenario

- A portfolio site arranges case study images in a responsive grid. On hover, captions slide in, and keyboard users toggle the same overlay with focus states.

## Examples

```css
.gallery {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(12rem, 1fr));
}

.gallery img {
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  border-radius: 0.75rem;
  transition: transform 200ms ease;
}

.gallery figure:focus-within img,
.gallery figure:hover img {
  transform: scale(1.03);
}
```

## Follow-up

- [ ] Build an image gallery with lightbox triggers using only CSS for layout and transitions.
- [ ] Add responsive captions that appear on hover/focus and remain accessible to keyboard users.
- [ ] Experiment with CSS columns or masonry techniques for irregular image sizes.
