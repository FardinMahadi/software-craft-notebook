---
title: AI Note-Taking Guidelines
last_reviewed: 09-11-2025
---

# AI Operating Guide for the Knowledge Base

Follow these rules whenever you create or update study material in `docs/`.

## 1. Workspace Structure

- All knowledge artifacts live under `docs/`.
- Domains: `domains/<discipline>/<topic>/` (e.g., `domains/web/frontend/react/`).
  - Required files: `overview.md`, `checklist.md`, `resources.md`, `labs/`, `concepts/`.
  - Concept notes use optional two-digit prefixes (`10-introduction.md`) when ordering matters.
  - Labs live in `labs/<slug>.md` with goal, tasks, deliverables.
- Shared principles belong in `docs/foundations/`.
- Skills planning: `docs/skills/`.
- Playbooks (including this file): `docs/playbooks/prompts/`.
- Daily notes: `docs/notes/YYYY-MM-DD-topic.md`.

## 2. Writing Constraints

- Keep individual Markdown files short (target ≤400 words; split when larger).
- Use ASCII characters; prefer straight quotes.
- Headings: start with `#`/`##` contextually (`#` reserved for file title).
- Sections to include in concept notes:
  - Quick summary/context.
  - Key ideas or bullet lists.
  - A real-world scenario describing how the concept shows up in practice (impact before/after).
  - Code snippets fenced with language.
  - “Practice Prompts” or next actions.
- Reference official sources (MDN, React docs, etc.) inline when relevant.
- When adding code, ensure formatting is clean and consistent with repo style.

## 3. Standard Workflows

### Adding a New Module

1. Create folder `domains/<discipline>/<topic>/`.
2. Add `overview.md` with scope, objectives, success criteria.
3. Create subfolders `concepts/` and `labs/`, plus `checklist.md` and `resources.md`.
4. Populate at least one concept note and checklist scaffold before closing the task.
5. Update `docs/README.md` or roadmap files only if structure changes.

### Extending an Existing Module

1. Review current `overview.md`, `checklist.md`, and `resources.md`.
2. Create new concept files with the next sequential number.
3. Update `resources.md` if new authoritative references are used (keep list <20 items).
4. Modify `checklist.md` only when tasks are completed or new ones are required.
5. If labs are added, update checklist and notes to reference them.

### Daily Notes & Reflections

- Use `docs/notes/YYYY-MM-DD-topic.md` for raw study sessions (sections: Context, Key Takeaways, Commands/Snippets, Open Questions).
- Summarize progress weekly/monthly in `docs/playbooks/reflections/`.
- Link back to module concept files when a daily note becomes evergreen knowledge.

## 4. Content Quality

- Extract information from official documentation (React, Node, MongoDB, etc.) and summarize in your own words.
- Highlight conceptual understanding, not just copy-pasted steps.
- Prefer bullet lists and concise paragraphs; avoid large walls of text.
- Keep explanations easy to understand; define jargon before using it and favor plain language.
- Include practice prompts or TODOs to reinforce learning.
- When referencing labs or checklists, keep wording actionable and binary (“done/not done”).

## 5. Housekeeping

- Before writing, run `git status` to confirm the working tree is clean or understand existing changes.
- Do not modify unrelated folders/projects while updating docs.
- When touching checklists, mark items `[x]` only after evidence exists in notes or labs.
- Archive outdated docs instead of deleting: move to `archive/` and note the status at the top of the file.
- Keep commit messages descriptive (e.g., “Add React quick start concepts”).

## 6. MERN Coverage Targets

Ensure future modules align with the roadmap:

- Frontend: HTML, CSS, Tailwind, JS fundamentals, React (basics → patterns).
- Backend: Node runtime, Express core, MongoDB basics.
- DevOps: Delivery pipelines, monitoring, operational excellence.
- Mobile: Native or cross-platform experience design and delivery.
- Data: Analytics engineering, ML fundamentals, data governance.

When starting a new topic, verify it appears in the relevant roadmap entry in `docs/skills/roadmap/` and link new artifacts accordingly.

---

Use this guide as the authoritative checklist for any AI-assisted note taking. Update `last_reviewed` when rules change.\*\*\*
