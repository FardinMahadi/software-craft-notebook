---
title: Modules, Tooling & Build Pipeline
status: draft
last_reviewed: 09-11-2025
---

# Modules, Tooling & Build Pipeline

## ES Modules

- Use `import`/`export` syntax; default export (`export default`) vs named exports (`export const helper = () => {}`).
- Prefer named exports for tooling transparency; default export for primary component/file entry.
- Dynamic imports (`const module = await import("./chunk.js")`) enable code splitting.

## Module Resolution

- Relative paths (`./utils.js`) vs bare specifiers (`react`); bundlers resolve bare specifiers via `node_modules`.
- Configure path aliases (e.g., Vite `@/`) for large projects but keep consistent across tooling.

## Bundlers & Transpilers

- React projects use Vite, Webpack, Parcel, or Next.js to transpile JSX (`@babel/preset-react` or SWC).
- Understand tree-shaking: export only necessary code and avoid side-effectful modules.
- Polyfills handled via bundler config or core-js; evaluate targets with Browserslist.

## Package Management

- `package.json` defines dependencies (`dependencies`, `devDependencies`) and scripts (`npm run dev`).
- Use lockfiles (`package-lock.json`, `pnpm-lock.yaml`) for deterministic installs.
- Keep scripts small; offload complex tasks to dedicated tooling config files.

## Linting & Formatting

- ESLint enforces code standards; configure with plugins like `eslint-plugin-react`, `eslint-plugin-import`.
- Prettier handles formatting; integrate with lint-staged or editor on-save hooks.
- Configure TypeScript declarations or JSDoc for type hints when needed.

## Environment Variables

- Use `.env` files with prefixes required by bundler (e.g., `VITE_`, `NEXT_PUBLIC_`).
- Never commit secrets; rely on deployment platform secret stores.
- Access via `import.meta.env` (Vite) or `process.env` (Node/Next).

## Practice Prompts

- Create a small utility library using named exports and consume it from a React component.
- Configure ESLint + Prettier in a sandbox project and document the command to run checks.
- Implement dynamic imports for a heavy chart component and verify the bundle splits in build output.

---

**Notes**

- Revisit latest bundler docs (Vite, Next.js, Webpack 5) for updates on path aliases and environment variable handling.
- Confirm tree-shaking guidance for CommonJS vs ES Module packages when linking to references.
