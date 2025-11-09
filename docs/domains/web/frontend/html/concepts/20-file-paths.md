# HTML File Paths

## Why It Matters

- Correct paths ensure browsers load images, stylesheets, and scripts without errors.
- Understanding relative vs. absolute paths prevents broken links during deployments.
- Predictable structures make collaboration easier as projects grow.

## Core Ideas

- **Absolute URLs** include the protocol (`https://example.com/assets/logo.png`) and work from any page.
- **Root-relative paths** start with `/` and resolve from the site root (`/assets/logo.png`).
- **Relative paths** depend on the current file location (`../images/logo.png`).
- `../` moves up one directory, while `./` references the current folder (often omitted).
- Build pipelines may rewrite paths, so keep a clear asset architecture (`assets/`, `css/`, `js/`).

## Real-World Scenario

- During a product launch, marketing hosts landing pages on a CDN. Using root-relative paths lets them deploy to different subdomains without editing every asset reference, and a quick path audit prevents embarrassing broken images on launch day.

## Examples

```html
<img src="/img/team.jpg" alt="Team meeting" />
<link rel="stylesheet" href="../styles/base.css" />
<script src="scripts/app.js" type="module"></script>
```

## Follow-up

- [ ] Map your project’s folder structure and document which paths are absolute vs. relative.
- [ ] Break a path intentionally, reload the page, and inspect the network panel to learn 404 debugging.
- [ ] Confirm filenames match case sensitivity requirements on production servers.

---

title: HTML File Paths
status: draft
last_reviewed: 09-11-2025

---
