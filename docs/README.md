# Knowledge Base Overview

This directory holds the curated knowledge for software craft. Everything is broken into small, linkable files so information stays easy to evolve and cross-reference.

## Directory Map

- `foundations/` – enduring concepts that apply across domains (architecture, patterns, CS basics, quality practices).
- `domains/` – specialised material grouped by discipline:
  - `web/`
  - `mobile/`
  - `backend/`
  - `devops/`
  - `data/`
- `skills/` – goal-setting tools: milestones, skills matrices, roadmaps, progression trackers.
- `playbooks/` – workflows and rituals (study systems, prompts, retrospectives, schedules).
- `resources/` – curated external references, bibliographies, glossaries.
- `tooling/` – environment setup notes, troubleshooting guides, automation instructions.
- `notes/` – dated capture log for transient insights before promotion.
- `templates/` – reusable skeletons for concepts, labs, checklists, and planning artefacts.

Each subdirectory includes a `README.md` or `overview.md` describing scope, conventions, and cross-links. When you create a new folder, start with one of these orientation files.

## Working Agreement

1. Keep files concise (<500 words). Split into subfolders when a topic expands.
2. Use kebab-case names. Reserve two-digit numeric prefixes (`10-intro.md`) only when ordering matters.
3. Add YAML front matter where practical:
   ```
   ---
   status: draft
   updated: 2025-11-09
   tags: [css, layout]
   links:
     - label: Related Lab
       path: ../labs/layout-refactor.md
   ---
   ```
4. Cross-link aggressively between foundations and domain notes to emphasise reuse.
5. When a file becomes stale, move it to `archive/` with `status: archived` and note why.

## Update Cadence

- **Weekly:** promote high-signal notes from `notes/` into the relevant domain or foundation folder and close out checklists.
- **Monthly:** revisit `skills/` to adjust roadmaps, refresh playbooks, and prune resources.
- **Quarterly:** audit naming consistency, simplify dense directories, and ensure templates still match how you work.

For change tracking, log significant shifts in `docs/CHANGELOG.md` and reference the commit hash for traceability.
