# Forms & Inputs

## Why It Matters

- Forms capture user intent, so clarity and accessibility directly impact conversions.
- Semantic markup unlocks native validation, helpful mobile keyboards, and automation.
- Well-structured forms reduce the need for custom JavaScript fixes.

## Core Ideas

- Pair every input with a `<label>` using `for`/`id`, or wrap the input inside the label.
- Group related fields with `<fieldset>` and `<legend>` (radio groups, wizards).
- Provide helper text via elements referenced by `aria-describedby`.
- Mark required fields with `required` and explain requirements in text, not color alone.
- Use input types (`email`, `tel`, `url`, `number`, `date`) to trigger native validation and device-appropriate keyboards.
- Offer descriptive error messaging near the input and tie it to the control for screen readers.

## Real-World Scenario

- A subscription form converts poorly because mobile users mistype email addresses. Switching the input type to `email`, adding concise labels, and surfacing inline helper text reduces bounce rates and support tickets.

## Examples

```html
<form aria-describedby="signup-help">
  <p id="signup-help">Create your account to access the dashboard.</p>
  <fieldset>
    <legend>Contact Details</legend>
    <label for="email">Email</label>
    <input
      id="email"
      name="email"
      type="email"
      autocomplete="email"
      required
      aria-describedby="email-hint"
    />
    <p id="email-hint">We’ll send updates to this address.</p>
  </fieldset>
  <button type="submit">Sign up</button>
</form>
```

## Follow-up

- [ ] Audit existing forms to ensure every control has a label and helper text where needed.
- [ ] Document error messaging patterns, including placement and ARIA attributes.
- [ ] Decide which validation rules rely on native browser constraints vs. custom logic.
---
title: Forms & Inputs
status: draft
last_reviewed: 09-11-2025
---

