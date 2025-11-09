# Images, Media & Embeds

## Why It Matters

- Rich media boosts storytelling but can hurt performance if unoptimized.
- Accessible markup ensures captions, transcripts, and alternative text reach all users.
- Responsive assets prevent giant downloads on mobile devices.

## Core Ideas

- Use `<picture>` and `srcset`/`sizes` to serve appropriate image resolutions; provide fallback formats.
- Wrap visuals that need attribution in `<figure>` with `<figcaption>`.
- `<video controls>` requires captions via `<track kind="captions">`; offer transcripts for longer content.
- External embeds (`<iframe>`, `<embed>`) need descriptive `title`, security-conscious `sandbox`, and often `loading="lazy"`.
- Defer below-the-fold assets with `loading="lazy"` where supported.

## Real-World Scenario

- A conference site embeds keynote videos from a streaming platform and showcases speaker photos. Responsive image sources keep thumbnails crisp without punishing mobile users, while caption tracks and transcripts let attendees revisit content without audio.

## Examples

```html
<figure>
  <picture>
    <source
      srcset="/img/hero@2x.webp 2x, /img/hero.webp 1x"
      type="image/webp"
    />
    <img
      src="/img/hero.jpg"
      alt="Product team reviewing a roadmap on a whiteboard"
      loading="lazy"
    />
  </picture>
  <figcaption>Quarterly planning session for the product roadmap.</figcaption>
</figure>

<video controls preload="metadata" poster="/img/keynote-poster.jpg">
  <source src="/video/keynote.mp4" type="video/mp4" />
  <track
    kind="captions"
    src="/captions/keynote-en.vtt"
    srclang="en"
    label="English captions"
    default
  />
  Sorry, your browser does not support embedded videos. Download the
  <a href="/video/keynote.mp4">MP4</a>.
</video>
```

## Follow-up

- [ ] Build responsive image sets with `srcset` and verify the correct variant loads in dev tools.
- [ ] Add captions/tracks to existing videos and confirm they appear in the controls.
- [ ] Document fallback and security settings for third-party embeds used in your projects.
---
title: Images, Media & Embeds
status: draft
last_reviewed: 09-11-2025
---


