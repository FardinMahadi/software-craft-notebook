# HTML Iframes

## Why It Matters

- `<iframe>` embeds external pages such as maps, videos, or dashboards directly into your layout.
- Proper configuration protects performance and privacy when loading third-party content.

## Core Ideas

- Required attributes: `src` for the URL and `title` for accessibility; control size via CSS or `width`/`height`.
- `loading="lazy"` defers off-screen frames; `allowfullscreen` enables full-screen mode for media.
- Use `sandbox` to restrict permissions and `referrerpolicy` to limit what information is shared.
- Only embed trusted sources; third-party content can inject tracking or mixed content warnings.

## Real-World Scenario

- A customer portal embeds analytics dashboards from an external BI tool. By adding a restrictive sandbox, lazy loading, and a clear title, the team keeps the page performant while meeting security requirements.

## Examples

```html
<div class="map-embed">
  <iframe
    src="https://maps.example.com/embed/location"
    title="Campus map"
    loading="lazy"
    sandbox="allow-scripts allow-same-origin"
    allowfullscreen
  ></iframe>
</div>
```

```css
.map-embed iframe {
  width: 100%;
  aspect-ratio: 4 / 3;
  border: 0;
}
```

## Follow-up

- [ ] Embed a video or map within a layout and ensure it scales responsively.
- [ ] Experiment with `sandbox` flags to understand how they restrict embedded content.
- [ ] Review privacy policies for third-party embeds and document what data is shared.
---
title: HTML Iframes
status: draft
last_reviewed: 09-11-2025
---

