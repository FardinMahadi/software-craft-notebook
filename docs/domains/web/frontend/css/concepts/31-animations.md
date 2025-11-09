# CSS Animations

## Why It Matters

- Keyframe animations create multi-step motion without JavaScript.
- Thoughtful motion guides attention and makes interfaces feel alive.

## Core Ideas

- Define animations with `@keyframes` and apply them using `animation-name`, `animation-duration`, and related properties.
- Control loops, direction, and end states via `animation-iteration-count`, `animation-direction`, and `animation-fill-mode`.
- Animate performant properties (transform, opacity) and offer reduced-motion alternatives.

## Real-World Scenario

- A loading indicator pulses while data loads. When `prefers-reduced-motion` is detected, the animation stops so sensitive users aren’t overwhelmed.

## Examples

```css
@keyframes pulse {
  0%,
  100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
}

.pulse {
  animation: pulse 1.5s ease-in-out infinite;
}

@media (prefers-reduced-motion: reduce) {
  .pulse {
    animation: none;
  }
}
```

## Follow-up

- [ ] Create a loading indicator that loops using keyframes.
- [ ] Experiment with `animation-fill-mode` to control final states after animation completes.
- [ ] Provide reduced-motion variants so animations respect user preferences.
---
title: CSS Animations
status: draft
last_reviewed: 09-11-2025
---

