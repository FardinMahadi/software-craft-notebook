---
title: Computer Code Elements
status: draft
last_reviewed: 09-11-2025
---

# Computer Code Elements

## Why It Matters

- Code snippets, keyboard shortcuts, and terminal output need clear semantics for readability and accessibility.
- Proper elements aid screen readers and enable consistent styling across documentation.

## Core Ideas

- `<code>` marks inline code; wrap block examples with `<pre><code>`.
- `<kbd>` represents keyboard input, `<samp>` shows sample output, and `<var>` highlights variables/placeholders.
- `<pre>` preserves spacing and line breaks—pair with monospace fonts via CSS.
- Syntax highlighting libraries often target these elements, so semantic markup makes them easier to extend.

## Real-World Scenario

- A developer handbook documents CLI workflows. Using `<kbd>` for shortcuts, `<samp>` for terminal output, and `<code>` for commands keeps instructions scannable and screen-reader friendly, reducing onboarding time for new engineers.

## Examples

```html
<p>Run <code>npm install</code> to install dependencies.</p>
<pre><code>
function add(a, b) {
  return a + b;
}
</code></pre>
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save and expect <samp>Saved!</samp> in the status bar.</p>
<p>Use <var>filename</var> as a placeholder in documentation.</p>
```

## Follow-up

- [ ] Document a CLI workflow using `<kbd>` for shortcuts and `<samp>` for terminal output.
- [ ] Compare rendering differences between inline `<code>` and block-level `<pre><code>`.
- [ ] Apply consistent styling (monospace font, background) via CSS utilities or components.
