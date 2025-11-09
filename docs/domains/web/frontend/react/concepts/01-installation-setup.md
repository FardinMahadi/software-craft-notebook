---
title: Installation & Environment Setup
status: draft
last_reviewed: 09-11-2025
---

# Installation & Environment Setup

Reference: React docs “Installation”, “Creating a React App”, “Build a React App from Scratch”, “Add React to an Existing Project”, “Editor Setup”, “Using TypeScript”, and “React Developer Tools”.

## Project Scaffolding Options
- **Framework-first**: use Vite, Next.js, Remix, Expo Router, etc., for batteries-included DX (recommended by React team).
- **Manual bundler**: configure bundlers like Webpack or Parcel for full control; follow “Build a React App from Scratch” guide if needed.
- **Embed in existing apps**: add React via npm dependencies to existing server-rendered or multi-page apps; hydrate islands progressively.

## Minimal Tooling Stack
1. Node.js ≥ 18 (use `nvm` to switch versions).
2. Package manager (npm, pnpm, yarn).
3. Development server (Vite / Next.js) with hot module replacement.
4. Build step producing optimized bundles for production.

## Editor Configuration
- Install Prettier + ESLint with React plugins.
- Enable JSX/TSX syntax highlighting and auto-imports.
- Configure editor to format on save and respect `.editorconfig`.

## TypeScript Integration
- Create projects with TS templates (`npm create vite@latest my-app -- --template react-ts`).
- Add `tsconfig.json` with JSX settings (`"jsx": "react-jsx"`).
- Type component props explicitly; use React’s utility types (`React.FC`, `React.ComponentProps`).

## React Developer Tools
- Browser extension for Chrome/Firefox records component trees, props, and hooks.
- Use Profiler tab to analyze render timings and re-renders.

## Adding React to Legacy Projects
- Serve the root container element (`<div id="root"></div>`) and mount React with `createRoot`.
- Gradually wrap legacy widgets in React components; interoperate via props or custom events.

## Practice Prompts
- Scaffold a new React project with Vite (JS) and another with TS; compare DX and config files.
- Integrate React into an existing static site by mounting a component into a single page.
- Configure ESLint + Prettier and Document the rules enforced in the project README.

