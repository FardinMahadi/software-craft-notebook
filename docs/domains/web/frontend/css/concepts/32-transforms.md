# CSS Transforms

## Why It Matters

- Transforms move, scale, rotate, and skew elements without affecting surrounding layout.
- They power hover effects, animations, and 3D illusions in a performant way.

## Core Ideas

- 2D transforms: `translate`, `scale`, `rotate`, `skew`; combine multiple functions in one declaration.
- 3D transforms: `rotateX`, `rotateY`, `translateZ`; add `perspective` on the parent for depth.
- Adjust `transform-origin` to change the pivot point (default is element center).
- Pair transforms with transitions for smooth motion.

## Real-World Scenario

- A card component lifts slightly on hover using `transform: translateY(-4px) scale(1.02);`, creating a tactile feel without reflow.

## Examples

```css
.card:hover {
  transform: translateY(-4px) scale(1.02);
}

.flip {
  transform: rotateY(180deg);
  transform-origin: center;
}

.scene {
  perspective: 1000px;
}
```

## Follow-up

- [ ] Create hover effects using subtle scale and translate transforms.
- [ ] Pair transforms with transitions for smooth animations.
- [ ] Experiment with 3D transforms and perspective to build flip cards.
---
title: CSS Transforms
status: draft
last_reviewed: 09-11-2025
---

