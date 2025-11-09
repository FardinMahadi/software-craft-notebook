# Accessibility Checks

## Why It Matters

- Inclusive experiences require ongoing checks beyond semantic HTML.
- Early accessibility reviews prevent costly fixes right before launch.
- Consistent auditing builds empathy and trust with diverse users.

## Core Ideas

- Maintain heading hierarchy without skipping levels; use a single `<h1>` per page.
- Ensure interactive elements (`button`, `a`, `input`, `summary`) are keyboard accessible and have visible focus states.
- Use ARIA attributes to clarify when native semantics fall short—never duplicate roles unnecessarily.
- Meet color contrast ratios (4.5:1 for body text, 3:1 for large/bold text) and document exceptions.
- Provide skip links (`<a href="#main" class="skip-link">Skip to content</a>`) for keyboard users.
- Test with screen readers (NVDA, VoiceOver) and automated tools (axe, Lighthouse) throughout development.

## Real-World Scenario

- During a QA review, a signup form fails WCAG contrast requirements. By running axe and VoiceOver checks early, the team updates color tokens and focus outlines before launching marketing campaigns, avoiding negative feedback from new customers.

## Examples

```html
<a class="skip-link" href="#main">Skip to main content</a>

<main id="main">
  <h1>Account Settings</h1>
  <button type="button">Update password</button>
</main>
```

## Follow-up

- [ ] Add automated accessibility scans (axe CLI, Lighthouse) to your CI pipeline.
- [ ] Run a manual keyboard walkthrough of each page; note and fix any traps.
- [ ] Record accessibility findings in retrospectives and track remediation tasks.
---
title: Accessibility Checks
status: draft
last_reviewed: 09-11-2025
---


