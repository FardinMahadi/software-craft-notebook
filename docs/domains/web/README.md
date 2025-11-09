# Web Domain Overview

The web track covers client-side foundations, UI engineering practices, and supporting tooling. Each topic lives in a self-contained bundle so concepts, labs, and resources stay tightly scoped.

## Layout

- `frontend/html/`
- `frontend/css/`
- `frontend/javascript/`
- `frontend/react/`
- `frontend/tailwind/`
- `frontend/typescript/`

Every topic folder contains:

- `overview.md` – scope, objectives, success criteria.
- `concepts/` – bite-sized explanations (`10-introduction.md`, `20-layout.md`, etc.).
- `labs/` – guided exercises with success metrics.
- `checklist.md` – binary completion items with optional front matter.
- `resources.md` – curated references (≤20 links, each annotated).
- `code/` (optional) – larger code samples kept outside Markdown when needed.

## Contribution Practices

1. Apply YAML front matter to `overview.md`, `checklist.md`, and new concept files.
2. Keep numbering sequences contiguous. Reserve future slots with stub files if you know upcoming topics.
3. Cross-link to shared knowledge in `docs/foundations/` (e.g., performance, accessibility) instead of duplicating content.
4. Record experiments or implementations in `projects/` and reference them from the relevant concept or lab.
5. When a topic graduates (e.g., React basics → React patterns), add a note in `docs/CHANGELOG.md` and move older material to `archive/` if it no longer reflects current practice.

See `../README.md` for global conventions shared across all domains.
